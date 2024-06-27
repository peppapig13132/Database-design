# Gift Card for e-Commerce Project
:label: MySQL

Supporse `user` table is already defined.

`giftcard`
| id | user_id | giftcard_balance | created_at | updated_at |
| :-: | :-: | :-: | :-: | :-: |
| INT | INT | DECIMAL(10, 2) | DATETIME | DATETIME |
| 1 | 24 | 250 | 2024-06-27 12:09:18.608 | 2024-06-27 12:09:18.608 |

`giftcard_log`
| id | giftcard_id | change_amount | category | reference_id | status | created_at | updated_at |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| INT| INT| INT | ENUM(PUCHARSE, CONSUME) | INT | ENUM(DRAFT, SUCCESS, FAILED) | DATETIME | DATETIME |
