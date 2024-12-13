# 데이터 애널리스트 코딩 테스트

## Part 1: SQL 과제

다음 테이블 구조를 가진 이커머스 데이터베이스가 주어진다고 가정합시다:

```sql
-- 고객 정보
customers (
    customer_id INT,
    name VARCHAR(100),
    email VARCHAR(100),
    join_date DATE,
    country VARCHAR(50)
)

-- 주문 정보
orders (
    order_id INT,
    customer_id INT,
    order_date DATE,
    total_amount DECIMAL(10,2),
    status VARCHAR(20)
)

-- 주문 상세
order_items (
    order_id INT,
    product_id INT,
    quantity INT,
    unit_price DECIMAL(10,2)
)

-- 제품 정보
products (
    product_id INT,
    product_name VARCHAR(100),
    category VARCHAR(50),
    unit_cost DECIMAL(10,2)
)
```

### SQL 문제:

1. 2023년 월별 총 매출액과 전월 대비 증감률을 계산하세요.

2. 각 고객의 첫 구매부터 두 번째 구매까지 걸린 평균 일수를 계산하세요. 
   - 아직 두 번째 구매가 없는 고객은 제외
   - 국가별로 그룹화하여 평균 일수가 긴 순서대로 정렬

3. 다음 조건을 만족하는 충성 고객을 찾아주세요:
   - 최근 6개월 동안 매월 1회 이상 구매
   - 총 구매금액이 상위 10% 이상
   - 반품 비율이 5% 미만
   결과는 고객ID, 이름, 총 구매횟수, 총 구매금액을 포함해야 합니다.

## Part 2: Python 분석 과제

git repo에 제공된 데이터셋(ecommerce_data.zip)을 사용하여 다음 분석을 수행해주세요:

### 1. 데이터 전처리 및 기초 분석
- 결측치 처리 및 이상치 탐지
- 기본적인 통계 지표 계산
- 데이터 품질 이슈 파악 및 해결 방안 제시

### 2. 고객 세그먼테이션 분석
- RFM 분석을 통한 고객 세그먼테이션 수행
- 각 세그먼트별 특성 파악
- 시각화를 통한 세그먼트 분포 표현

### 3. 제품 연관성 분석
- 장바구니 분석을 통한 제품 간 연관성 파악
- 상위 10개 연관 규칙 도출
- 시각화를 통한 결과 표현

## 제출 형식:
1. SQL 쿼리 파일 (.sql)
2. Python 분석 코드 (.ipynb 또는 .py)
3. 분석 결과 리포트 (PDF)
   - 데이터 전처리 과정 설명
   - 주요 발견 사항
   - 분석을 통해 발견한 인사이트

## 평가 기준:
- 코드 품질 및 효율성
- 분석 방법의 적절성
- 결과 해석의 타당성
- 시각화의 명확성
- 문제 해결 접근 방식
