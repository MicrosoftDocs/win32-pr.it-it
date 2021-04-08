---
title: Funzione MpFreeMemory (MpClient. h)
description: Libera la memoria per malware Protection Manager.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpFreeMemory
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741010"
---
# <a name="mpfreememory-function"></a>MpFreeMemory (funzione)

Libera la memoria per malware Protection Manager. Tutti i buffer allocati e restituiti dalle funzioni Malware Protection devono essere liberati dal chiamante tramite questa funzione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMemory* \[ in\]
</dt> <dd>

Tipo: **PVOID**

Puntatore alla memoria allocata da una funzione di protezione da malware.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Per facilitare la gestione della memoria per i client, malware Protection Manager definisce anche le macro per liberare memoria associata alle varie strutture restituite dalle funzioni di malware Protection. Le macro seguenti sono definite nel file di intestazione mpmemfree. h:



| Nome                            | Descrizione                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| \_informazioni MPRESOURCE \_ gratuite          | Libera le [**\_ informazioni MPRESOURCE**](mpresource-info.md)allocate.                  |
| \_informazioni MPTHREAT \_ gratuite            | Libera le [**\_ informazioni MPTHREAT**](mpthreat-info.md)allocate.                      |
| MPTHREAT \_ informazioni localizzate \_ \_ gratuite | Libera le [**\_ \_ informazioni localizzate MPTHREAT**](mpthreat-localized-info.md)allocate. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**\_informazioni MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**\_informazioni MPTHREAT**](mpthreat-info.md)
</dt> <dt>

[**\_informazioni localizzate MPTHREAT \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





