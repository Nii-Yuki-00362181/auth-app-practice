# auth-app-practice

## 概要

COACHTECH 教材 Tutorial 10-1「認証機能 ハンズオン演習」で作成した成果物です。

Laravel Fortifyを使って、ユーザー登録、ログイン、ログアウト、認証保護されたダッシュボード画面を作成したWedアプリケーションです。

## 使用技術

- PHP 8.x
- Laravel 10.x
- Laravel Fortify（認証）
- MySQL（Docker, Laravel Sail）

## 学んだこと

- Laravel Fortify を使ったユーザー登録、ログイン、ログアウトのバックエンド処理の仕組み
- RouteServiceProvider、config/fortify.php でログイン後のリダイレクト先を統一管理する方法
- authミドルウェアを使って特定ルートを保護し、未認証ユーザーをログインページにリダイレクトさせる制御

## 動作確認

- sail up -d で環境を起動
- sail artisan migrate を実行
- ブラウザで http://localhost/register にアクセスしてユーザー登録を実行
- 登録成功後、自動的に /dashboard にリダイレクトされユーザー名が表示されることを確認
- 「ログアウト」ボタンを押すとログアウトされ、ウェルカムページへリダイレクトされることを確認
- 未ログイン状態で http://localhost/dashboard に直接アクセスすると、/login へ強制リダイレクトされることを確認
- 登録したアカウントで /login から再ログインできることを確認
