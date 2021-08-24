---
title: Enumerazione DODownloadCostPolicy
description: Specifica l'ID delle opzioni dei criteri di costo associate **alla DODownloadProperty_CostPolicy** proprietà .
keywords:
- Enumerazione DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 763042ed6d0df6fa287fbe66d23528a199a73041cb3500c6a2812e6db86cb698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677881"
---
# <a name="dodownloadcostpolicy-enumeration"></a>Enumerazione DODownloadCostPolicy

**L'enumerazione DODownloadCostPolicy** specifica l'ID delle opzioni dei criteri di costo associate alla **DODownloadProperty_CostPolicy** proprietà .

## <a name="syntax"></a>Sintassi

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a>Costanti

| Requisito | Valore |
|-|-|
| DODownloadCostPolicy_Always | Il download viene eseguito indipendentemente dal costo. |
| DODownloadCostPolicy_Unrestricted | Il download viene eseguito a meno che non imposizioni di costi o limiti di traffico. |
| DODownloadCostPolicy_Standard | Il download viene eseguito a meno che non sia soggetto a un supplemento o a un esaurimento quasi. |
| DODownloadCostPolicy_NoRoaming | Il download viene eseguito a meno che la connettività non sia soggetta a costi di roaming. |
| DODownloadCostPolicy_NoSurcharge | Il download viene eseguito a meno che non sia soggetto a un supplemento. |
| DODownloadCostPolicy_NoCellular | Il download viene eseguito a meno che la rete non sia nella rete cellulare. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | DeliveryOptimizationDownloadTypes.h |
