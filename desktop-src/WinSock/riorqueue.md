---
description: Specifica un descrittore di socket utilizzato dalle richieste di invio e ricezione con le estensioni I/O registrate di Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344741"
---
# <a name="rio_rq"></a>RIO \_ RQ

Il typedef di **Rio \_ RQ** specifica un descrittore di socket usato dalle richieste di invio e ricezione con le estensioni i/O registrate di Winsock.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**RIO \_ RQ**
</dt> <dd>

Tipo di dati che specifica un descrittore di socket utilizzato dalle richieste di invio e ricezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le estensioni I/O registrate di Winsock operano principalmente su un oggetto **Rio \_ RQ** anziché su un socket. Un'applicazione ottiene un oggetto **Rio \_ RQ** per un socket esistente usando la funzione [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) . Il socket di input deve essere stato creato chiamando la funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con il flag WSA del flag **\_ \_ Rio** impostato nel parametro *dwFlags* .

Dopo aver ottenuto un oggetto **Rio \_ RQ** , il descrittore di socket sottostante rimane valido. Un'applicazione può continuare a usare il socket sottostante per impostare ed eseguire query sulle opzioni del socket, emettere IOCTL e infine chiudere il socket.

> [!Note]  
> Ai fini dell'efficienza, l'accesso alle code di completamento ([**struct \_ CQ**](riocqueue.md) ) e le code di richiesta (struct di **Rio \_ RQ** ) non sono protette dalle primitive di sincronizzazione. Se è necessario accedere a una coda di completamento o di richiesta da più thread, l'accesso deve essere coordinato da una sezione critica, da un blocco Write reader sottile o da un meccanismo simile. Questo blocco non è necessario per l'accesso da un singolo thread. Thread diversi possono accedere a code di completamento/richieste separate senza blocchi. La necessità di sincronizzazione avviene solo quando più thread tentano di accedere alla stessa coda. La sincronizzazione è necessaria anche se più thread inviano e ricevono lo stesso socket perché le operazioni di invio e ricezione utilizzano la coda di richieste del socket.

 

Il typedef di [**Rio \_ RQ**](riocqueue.md) è definito nel file di intestazione *Mswsockdef. h* , che viene incluso automaticamente nel file di intestazione *mswsock. h* . Il file di intestazione *Mswsockdef. h* non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Mswsockdef. h (include mswsock. h)</dt> </dl> |



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

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
