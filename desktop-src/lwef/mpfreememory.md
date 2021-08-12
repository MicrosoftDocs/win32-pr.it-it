---
title: Funzione MpFreeMemory (MpClient.h)
description: Libera memoria per Malware Protection Manager.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Funzione MpFreeMemory legacy Windows dell'ambiente
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
ms.openlocfilehash: 806795cee45fcfe95473c0961106da074c1157b65ac5c19f5d4813c84865616a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247426"
---
# <a name="mpfreememory-function"></a>Funzione MpFreeMemory

Libera memoria per Malware Protection Manager. Tutti i buffer allocati e restituiti dalle funzioni di protezione da malware devono essere liberati dal chiamante che usa questa funzione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMemory* \[ Pollici\]
</dt> <dd>

Tipo: **PVOID**

Puntatore alla memoria allocata da una funzione di protezione da malware.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Per facilitare la gestione della memoria per i client, Malware Protection Manager definisce anche le macro per liberare la memoria associata a varie strutture restituite dalle funzioni di protezione da malware. Le macro seguenti sono definite nel file di intestazione mpmemfree.h:



| Nome                            | Descrizione                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| MPRESOURCE \_ INFO \_ FREE          | Libera un oggetto [**MPRESOURCE \_ INFO allocato.**](mpresource-info.md)                  |
| MPTHREAT \_ INFO \_ FREE            | Libera un oggetto [**MPTHREAT \_ INFO allocato.**](mpthreat-info.md)                      |
| MPTHREAT \_ LOCALIZED \_ INFO \_ FREE | Libera un OGGETTO [**MPTHREAT \_ LOCALIZED INFO \_ allocato.**](mpthreat-localized-info.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> <dt>

[**INFORMAZIONI SU \_ MPTHREAT**](mpthreat-info.md)
</dt> <dt>

[**INFORMAZIONI LOCALIZZATE MPTHREAT \_ \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





