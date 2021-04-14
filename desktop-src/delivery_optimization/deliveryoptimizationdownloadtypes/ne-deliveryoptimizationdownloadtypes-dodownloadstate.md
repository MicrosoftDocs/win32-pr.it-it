---
title: Enumerazione DODownloadState
description: Specifica l'ID dello stato di download corrente, che fa parte della struttura **DO_DOWNLOAD_STATUS** .
keywords:
- Enumerazione DODownloadState, DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518544"
---
# <a name="dodownloadstate-enumeration"></a>Enumerazione DODownloadState

L'enumerazione **DODownloadState** specifica l'ID dello stato di download corrente, che fa parte della struttura **DO_DOWNLOAD_STATUS** .

## <a name="syntax"></a>Sintassi

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a>Costanti

| Requisito | Valore |
|-|-|
| DODownloadState_Created | L'oggetto di download è stato creato ma non è ancora stato avviato. |
| DODownloadState_Transferring | Il download è in corso. |
| DODownloadState_Transferred | Il download viene trasferito e può essere riavviato scaricando un'altra parte del file. |
| DODownloadState_Finalized | Il download è finalizzato e non può essere riavviato. |
| DODownloadState_Aborted | Il download è stato interrotto. |
| DODownloadState_Paused | Il download è stato sospeso su richiesta o a causa di un errore temporaneo. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | DeliveryOptimizationDownloadTypes. h |
