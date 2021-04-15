---
title: Enumerazione DODownloadCostPolicy
description: Specifica l'ID delle opzioni dei criteri di costo associate alla proprietà **DODownloadProperty_CostPolicy** .
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
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400294"
---
# <a name="dodownloadcostpolicy-enumeration"></a>Enumerazione DODownloadCostPolicy

L'enumerazione **DODownloadCostPolicy** specifica l'ID delle opzioni dei criteri di costo associate alla proprietà **DODownloadProperty_CostPolicy** .

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
| DODownloadCostPolicy_Unrestricted | Il download viene eseguito solo se impone costi o limiti di traffico. |
| DODownloadCostPolicy_Standard | Il download viene eseguito a meno che non sia soggetto a un sovrapprezzo né a un esaurimento. |
| DODownloadCostPolicy_NoRoaming | Il download viene eseguito a meno che la connettività non sia soggetta a sovrapprezzi in roaming. |
| DODownloadCostPolicy_NoSurcharge | Il download viene eseguito a meno che non sia soggetto a un supplemento. |
| DODownloadCostPolicy_NoCellular | Il download viene eseguito a meno che la rete non sia attiva. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | DeliveryOptimizationDownloadTypes. h |
