---
description: Specifica un descrittore di socket utilizzato dalle richieste di invio e ricezione con le estensioni di I/O registrate di Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162b87d1ae320bfa0e74f08e5a0ef7493c053f39573249246e8b2884e74f599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993581"
---
# <a name="rio_rq"></a>RIO \_ RQ

Il **typedef \_ RQ RIO** specifica un descrittore di socket usato dalle richieste di invio e ricezione con le estensioni di I/O registrate di Winsock.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**RIO \_ RQ**
</dt> <dd>

Tipo di dati che specifica un descrittore di socket utilizzato dalle richieste di invio e ricezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le estensioni di I/O registrate di Winsock operano principalmente su un oggetto **\_ RQ RIO** anziché su un socket. Un'applicazione ottiene un **\_ RQ RIO** per un socket esistente usando la [**funzione RIOCreateRequestQueue.**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) Il socket di input deve essere stato creato chiamando la [**funzione WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con il flag **\_ \_ WSA FLAG RIO** impostato nel parametro *dwFlags.*

Dopo aver ottenuto un **oggetto \_ RQ RIO,** il descrittore del socket sottostante rimane valido. Un'applicazione può continuare a usare il socket sottostante per impostare ed eseguire query su opzioni socket, eseguire ioCTL e infine chiudere il socket.

> [!Note]  
> Ai fini dell'efficienza, l'accesso alle code di completamento (struct [**RIO \_ CQ)**](riocqueue.md) e alle code di richiesta (struct **\_ RQ RIO)** non è protetto dalle primitive di sincronizzazione. Se è necessario accedere a una coda di completamento o richiesta da più thread, l'accesso deve essere coordinato da una sezione critica, da un blocco di scrittura del lettore sottile o da un meccanismo simile. Questo blocco non è necessario per l'accesso da parte di un singolo thread. Thread diversi possono accedere a code di richieste/completamento separate senza blocchi. La necessità di sincronizzazione si verifica solo quando più thread tentano di accedere alla stessa coda. La sincronizzazione è necessaria anche se più thread inviano e ricevono sullo stesso socket perché le operazioni di invio e ricezione usano la coda di richieste del socket.

 

Il [**typedef \_ RQ RIO**](riocqueue.md) è definito nel file di intestazione *Mswsockdef.h* che viene automaticamente incluso nel file di intestazione *Mswsock.h.* Il file *di intestazione Mswsockdef.h* non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Mswsockdef.h (includere Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))
</dt> <dt>

[**RIOSEND**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
