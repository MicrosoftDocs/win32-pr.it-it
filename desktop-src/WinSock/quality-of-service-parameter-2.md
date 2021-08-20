---
description: Questa sezione elenca i parametri usati per la qualità del servizio (QoS).
ms.assetid: befbcf01-ecd2-4316-8e5e-889e918272cc
title: Parametro quality of service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214b185752ba058e8ebb42547e0c90e35f6a2fedf68640bd2cca00fd39d7b27e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927468"
---
# <a name="quality-of-service-parameter"></a>Parametro quality of service

Questa sezione elenca i parametri usati per la qualità del servizio (QoS).

``` syntax
#include <windows.h>
/* 
 *  values used for the QOSClassForward and QOSClassBackward
 *  field in struct ATM_QOS_CLASS_IE
 */
#define QOS_CLASS0                  0x00
#define QOS_CLASS1                  0x01
#define QOS_CLASS2                  0x02
#define QOS_CLASS3                  0x03
#define QOS_CLASS4                  0x04

typedef struct {
    UCHAR QOSClassForward;
    UCHAR QOSClassBackward;
} ATM_QOS_CLASS_IE;
```

 

 



