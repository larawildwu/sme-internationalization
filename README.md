# board-gender-diversity-firm-performance

Name: Lara Wild

## Research Question

How does board gender diversity affect firm performance?

## Hypotheses

- H1: Firms with higher board gender diversity exhibit higher firm performance.

## Theoretical Background

The hypothesis is derived from resource dependence theory and agency theory. From a resource dependence perspective, boards provide firms with valuable resources such as knowledge, advice, external networks, and legitimacy; therefore, gender-diverse boards may broaden the range of perspectives and resources available for strategic decision-making (Hillman & Dalziel, 2003). From an agency theory perspective, boards monitor management on behalf of shareholders; gender-diverse boards may strengthen monitoring quality and governance processes, for example through higher monitoring effort and committee participation by female directors (Adams & Ferreira, 2009). Prior empirical research suggests that board diversity can be positively associated with firm value, including Tobin’s Q (Carter, Simkins, & Simpson, 2003). However, the empirical evidence is not fully uniform: meta-analytic evidence shows mixed results across studies and contexts, although female board representation is often positively related to accounting-based performance measures (Post & Byron, 2015).

Hillman, A. J., & Dalziel, T. (2003). Boards of directors and firm performance: Integrating agency and resource dependence perspectives. Academy of Management Review, 28(3), 383–396.
Adams, R. B., & Ferreira, D. (2009). Women in the boardroom and their impact on governance and performance. Journal of Financial Economics, 94(2), 291–309.
Carter, D. A., Simkins, B. J., & Simpson, W. G. (2003). Corporate governance, board diversity, and firm value. Financial Review, 38(1), 33–53.
Post, C., & Byron, K. (2015). Women on boards and firm financial performance: A meta-analysis. Academy of Management Journal, 58(5), 1546–1571.

## Independent Variable: Board Gender Diversity

The independent variable is board gender diversity, measured as the share of female directors on the board.
Formula:
Board Gender Diversity = Number of Female Directors / Total Number of Directors
The variable will be constructed using BoardEx North America. Two BoardEx datasets are required:

| Dataset | Required variables | Purpose |
|---|---|---|
| Organizational Composition | `companyID`, `directorID`, `companyname`, `rolename`, `datestartrole`, `dateendrole`, `seniority` | Identifies which individuals served in which firm and role |
| Individual Profile Details | `directorID`, `gender` | Adds gender information for each individual |

The two datasets are merged using ticker directorID.

## Dependent Variable

The main dependent variable is operating firm performance, measured by EBIT scaled by total assets. EBIT is used because it captures a firm’s operating profitability before interest and taxes and is therefore less affected by differences in capital structure and tax environments. To make EBIT comparable across firms of different sizes, EBIT is scaled by total assets.
According to the Compustat variable document, EBIT is available as the Compustat data item EBIT, while total assets are measured by AT. Therefore, the main performance variable is calculated as:
Operating Performance = EBIT / AT


