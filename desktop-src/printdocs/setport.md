---
description: La funzione SetPort imposta lo stato associato a una porta della stampante.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Funzione SetPort (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e3414d0566203aa51d78c6b7d4b0463cee5765bae8c35c083a959088b6559df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234031"
---
# <a name="setport-function"></a>Funzione SetPort

La **funzione SetPort** imposta lo stato associato a una porta della stampante.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il nome del server di stampa a cui è connessa la porta. Impostare questo parametro su **NULL** se la porta si trova nel computer locale.

</dd> <dt>

*pPortName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il nome della porta della stampante.

</dd> <dt>

*dwLevel* \[ Pollici\]
</dt> <dd>

Specifica il tipo di struttura a cui punta il *parametro pPortInfo.*

Questo valore deve essere 3, che corrisponde a una struttura di [**dati PORT \_ INFO \_ 3.**](port-info-3.md)

</dd> <dt>

*pPortInfo* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura PORT INFO \_ \_ 3**](port-info-3.md) che contiene le informazioni sullo stato della porta da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Il chiamante della **funzione SetPort** deve essere in esecuzione come amministratore. Inoltre, se il chiamante è un Monitoraggio porte o Language Monitor, deve chiamare [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) per determinare l'cessazione della rappresentazione prima di chiamare **SetPort**.

Tutti i programmi che chiamano **SetPort** devono avere accesso SERVER \_ ACCESS ADMINISTER al server a cui è \_ connessa la porta.

Quando si imposta un valore di stato della porta della stampante con il valore di gravità PORT STATUS TYPE ERROR, lo \_ spooler di stampa interrompe l'invio \_ \_ di processi alla porta. Lo spooler di stampa riprende l'invio di processi alla porta quando lo stato della porta viene cancellato da un'altra chiamata a **SetPort**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetPortW** (Unicode) e **SetPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**INFORMAZIONI \_ SULLA \_ PORTA 3**](port-info-3.md)
</dt> </dl>

 

