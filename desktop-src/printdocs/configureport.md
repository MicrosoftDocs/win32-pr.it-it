---
description: La funzione ConfigurePort visualizza la finestra di dialogo port-configuration per una porta nel server specificato.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Funzione ConfigurePort (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dbc31de341c137e8baf729a468e8576684ccef8b0a860be898c9cb5a6af34217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950441"
---
# <a name="configureport-function"></a>Funzione ConfigurePort

La **funzione ConfigurePort** visualizza la finestra di dialogo port-configuration per una porta nel server specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server in cui è presente la porta specificata. Se questo parametro è **NULL,** la porta è locale.

</dd> <dt>

*hWnd* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre della finestra di dialogo port-configuration.

</dd> <dt>

*pPortName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome della porta da configurare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Prima di chiamare la **funzione ConfigurePort,** un'applicazione deve chiamare la [**funzione EnumPorts**](enumports.md) per determinare i nomi di porta validi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **ConfigurePortW** (Unicode) e **ConfigurePortA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




