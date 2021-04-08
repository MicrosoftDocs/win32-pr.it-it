---
description: La funzione seport imposta lo stato associato a una porta stampante.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Funzione seport (winspool. h)
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
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049968"
---
# <a name="setport-function"></a>Funzione seport

La funzione **seport** imposta lo stato associato a una porta stampante.

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

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il nome del server di stampa a cui è connessa la porta. Impostare questo parametro su **null** se la porta si trova nel computer locale.

</dd> <dt>

*pPortName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione zero che specifica il nome della porta stampante.

</dd> <dt>

*dwLevel* \[ in\]
</dt> <dd>

Specifica il tipo di struttura a cui punta il parametro *pPortInfo* .

Questo valore deve essere 3, che corrisponde a una struttura di dati [**Port \_ info \_ 3**](port-info-3.md) .

</dd> <dt>

*pPortInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**informazioni sulla porta \_ \_ 3**](port-info-3.md) che contiene le informazioni sullo stato della porta da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il chiamante della funzione **seport** deve essere eseguito come amministratore. Inoltre, se il chiamante è un monitor della porta o del linguaggio, deve chiamare [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) per interrompere la rappresentazione prima di chiamare la **porta**.

Tutti i programmi che chiamano la **porta** \_ di accesso al server devono disporre dell'accesso al server \_ per amministrare l'accesso al server a cui è connessa la porta.

Quando si imposta un valore di stato porta stampante con l' \_ errore tipo di stato porta valore gravità \_ \_ , lo spooler di stampa interrompe l'invio di processi alla porta. Lo spooler di stampa riprende l'invio di processi alla porta quando lo stato della porta viene cancellato da un'altra chiamata a **seport**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetPortW** (Unicode) e **seporta** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Informazioni sulla porta \_ \_ 3**](port-info-3.md)
</dt> </dl>

 

