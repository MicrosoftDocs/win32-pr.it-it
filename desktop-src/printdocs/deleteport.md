---
description: La funzione DeletePort Visualizza una finestra di dialogo che consente all'utente di eliminare un nome di porta.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: Funzione DeletePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232377"
---
# <a name="deleteport-function"></a>DeletePort (funzione)

La funzione **DeletePort** Visualizza una finestra di dialogo che consente all'utente di eliminare un nome di porta.

## <a name="syntax"></a>Sintassi


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il nome del server per cui la porta deve essere eliminata. Se questo parametro è **null**, viene eliminata una porta locale.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra padre della finestra di dialogo di eliminazione della porta.

</dd> <dt>

*pPortName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il nome della porta da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Un'applicazione può recuperare i nomi delle porte valide chiamando la funzione [**EnumPorts**](enumports.md) .

La funzione **DeletePort** restituisce un errore se una stampante è attualmente connessa alla porta specificata.

Il chiamante della funzione **DeletePort** deve avere \_ accesso al server \_ per amministrare l'accesso al server a cui è connessa la porta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **DeletePortW** (Unicode) e **DeletePortA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




