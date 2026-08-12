# Test full luồng: Deploy PocketBase Cloud từ GitHub Actions

Nguồn: https://pocketbasecloud.com/docs/ci-cd/deploying-from-github-actions

## Checklist

- [ ] 1. Khởi tạo git repo + tạo project frontend demo tối giản
- [ ] 2. `pb cloud login` + `pb cloud frontend deploy` lần đầu (sinh `pb.json`)
- [ ] 3. Commit `pb.json`
- [ ] 4. Tạo repo GitHub mới + push code
- [ ] 5. Lấy CLI access token từ portal PocketBase Cloud
- [ ] 6. Thêm secret `PB_TOKEN` vào GitHub repo (Settings → Secrets and variables → Actions)
- [ ] 7. Tạo `.github/workflows/deploy.yml`
- [ ] 8. Push workflow, theo dõi tab Actions → xác nhận deploy CI thành công
- [ ] 9. Test biến môi trường frontend (`VITE_API_URL`) qua build step
- [ ] 10. Test negative case: thiếu `PB_TOKEN`, sai `working-directory`
- [ ] 11. Test redeploy: push commit thứ 2, xác nhận CI/CD tự chạy lại

## Ghi chú môi trường
- `pb` CLI: đã cài (v0.3.2)
- `gh` CLI: chưa cài → tạo repo qua github.com
- Project demo: static/Vite site tối giản trong thư mục `web/`
