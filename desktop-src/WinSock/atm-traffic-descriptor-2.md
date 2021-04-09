---
description: In questa sezione viene elencato il descrittore di traffico ATM.
ms.assetid: 8d15af95-2003-416e-b3b0-a9201972a899
title: Descrittore traffico ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb841cea1cacd3a613162a7e7da779872eb7ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129223"
---
# <a name="atm-traffic-descriptor"></a>Descrittore traffico ATM

In questa sezione viene elencato il descrittore di traffico ATM.

``` syntax
typedef struct {
    ULONG PeakCellRate_CLP0;
    ULONG PeakCellRate_CLP01;
    ULONG SustainableCellRate_CLP0;
    ULONG SustainableCellRate_CLP01;
    ULONG MaxBurstSize_CLP0;
    ULONG MaxBurstSize_CLP01;
    BOOL  Tagging;
} ATM_TD;

typedef struct {
    ATM_TD Forward;
    ATM_TD Backward;
    BOOL   BestEffort;
} ATM_TRAFFIC_DESCRIPTOR_IE;
```

 

 



