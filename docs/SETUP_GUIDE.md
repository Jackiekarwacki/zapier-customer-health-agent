# 🚀 Quick Setup Guide

## Prerequisites Checklist

Before starting, ensure you have:

- [ ] **Zapier Professional Account** (required for multiple Zaps)
- [ ] **HubSpot Account** (free tier available)
- [ ] **Slack Workspace** (optional, for alerts)

## 5-Step Setup Process

### Step 1: Create Zapier Tables (15 minutes)
1. Go to zapier.com/app/tables
2. Create 3 tables:
   - **Health Scores** (main dashboard)
   - **Raw Data** (incoming events)
   - **VitalEdge Reports** (executive intelligence)

### Step 2: Set Up Data Collection (30 minutes)
Create 5 Zaps:
1. **HubSpot → Zapier Tables** (real CRM data)
2. **Schedule → Code → Tables** (simulated support data)
3. **Schedule → Code → Tables** (simulated usage data)
4. **Schedule → Code → Tables** (simulated plan data)
5. **Schedule → Code → Tables** (simulated onboarding data)

### Step 3: Configure Health Score Processing (20 minutes)
1. Create the main health scoring Zap
2. Add JavaScript code step for score calculation
3. Configure the weighted scoring algorithm
4. Set up automated health score updates

### Step 4: Set Up Alerts (15 minutes)
1. Create Slack notification Zap
2. Configure trigger conditions
3. Test alert system

### Step 5: Deploy Reporting (20 minutes)
1. Create executive reporting Zap
2. Configure weekly/monthly schedules
3. Test report generation

## 🎯 Success Metrics

After setup, you should see:
- ✅ Customer data flowing into Raw Data table
- ✅ Health scores calculating automatically
- ✅ Risk alerts triggering for critical customers
- ✅ Executive reports generating on schedule

## 🆘 Troubleshooting

### Common Issues:
1. **No data flowing**: Check Zap triggers and connections
2. **Health scores not calculating**: Verify JavaScript code syntax
3. **Alerts not sending**: Check Slack permissions
4. **Reports blank**: Verify table field mappings

### Getting Help:
- Check the detailed instructions in `zapier-customer-health-agent-instructions.md`
- Review example data in the `examples/` folder
- Test with sample webhook payloads

## 🔧 Customization

### Modify Scoring Weights:
Edit the JavaScript code in the health scoring Zap:
```javascript
const overallHealthScore = Math.min(
  (zapUsageScore * 0.25) +           // Adjust weights here
  (platformAdoptionScore * 0.225) +  
  (appConnectionsScore * 0.20) +     
  (planUtilizationScore * 0.20) +    
  (onboardingProgressScore * 0.20) + 
  (supportHealthScore * 0.125), 
  100
);
```

### Add New Data Sources:
1. Create new data collection Zap
2. Map to Raw Data table
3. Update health scoring algorithm
4. Test with sample data

---

**Total Setup Time: ~2 hours**

For detailed step-by-step instructions, see the complete guide in `zapier-customer-health-agent-instructions.md`. 