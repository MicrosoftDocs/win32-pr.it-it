---
title: Enumerazione DODownloadState
description: Specifica l'ID dello stato di download corrente, che fa parte DO_DOWNLOAD_STATUS **struttura** .
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
ms.openlocfilehash: 5df8f7b20c8cff3b905acec9852b26c9a5ee360645fddb1bec22990a8bb9daba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047139"
---
# <a name="dodownloadstate-enumeration"></a>Enumerazione DODownloadState

**L'enumerazione DODownloadState** specifica l'ID dello stato di download corrente, che fa parte DO_DOWNLOAD_STATUS **struttura.**

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
| DODownloadState_Created | L'oggetto di download viene creato ma non è ancora stato avviato. |
| DODownloadState_Transferring | Download in corso. |
| DODownloadState_Transferred | Il download viene trasferito e può essere avviato di nuovo scaricando un'altra parte del file. |
| DODownloadState_Finalized | Il download è finalizzato e non può essere avviato di nuovo. |
| DODownloadState_Aborted | Il download è stato interrotto. |
| DODownloadState_Paused | Il download è stato sospeso su richiesta o a causa di un errore temporaneo. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | DeliveryOptimizationDownloadTypes.h |
