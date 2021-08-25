---
description: La funzione LoadTCHAR viene chiamata dai monitoraggi per impostare una variabile stringa su una stringa tratta da una stringa di configurazione HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Funzione LoadTCHAR (Netmon.h)
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
ms.openlocfilehash: 2d85419485e2442f82c94948b832914fa30e44396f266eed10cd1545b4cc28ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890287"
---
# <a name="loadtchar-function"></a>Funzione LoadTCHAR

La **funzione LoadTCHAR** viene chiamata dai monitoraggi per impostare una variabile stringa su una stringa tratta da una stringa di configurazione HTML.

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

*pConfig* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio dal [metodo IMonitor::D oConfigure.](imonitor-doconfigure.md)

</dd> <dt>

*pVarName* \[ Pollici\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*ppszString* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore di stringa. Se viene trovato il nome della variabile richiesta, la stringa viene allocata e assegnata a questo puntatore. È responsabilità dell'utente liberare la memoria associata alla stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (se il nome della variabile è stato trovato e ha una stringa di lunghezza non zero), il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




