---
description: La funzione LoadTCHAR viene chiamata dai monitoraggi per impostare una variabile di stringa su una stringa eseguita da una stringa di configurazione HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Funzione LoadTCHAR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307721"
---
# <a name="loadtchar-function"></a>LoadTCHAR (funzione)

La funzione **LoadTCHAR** viene chiamata dai monitoraggi per impostare una variabile di stringa su una stringa eseguita da una stringa di configurazione HTML.

## <a name="syntax"></a>Sintassi


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConfig* \[ in\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .

</dd> <dt>

*pVarName* \[ in\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*ppszString* \[ out\]
</dt> <dd>

Puntatore a un puntatore di stringa. Se viene trovato il nome della variabile richiesta, la stringa viene allocata e assegnata a questo puntatore. È responsabilità dell'utente liberare la memoria associata alla stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (se il nome della variabile è stato trovato e ha una stringa di lunghezza diversa da zero), il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




