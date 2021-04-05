---
description: Specifica un descrittore di buffer registrato utilizzato con le estensioni I/O registrate di Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049767"
---
# <a name="rio_bufferid"></a>RIO \_ BUFFERID

Il **typedef \_ BUFFERID di Rio** specifica un descrittore di buffer registrato usato con le estensioni i/O registrate di Winsock.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**RIO \_ BUFFERID**
</dt> <dd>

Tipo di dati che specifica un descrittore di buffer registrato utilizzato con le richieste di invio e ricezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le estensioni I/O registrate di Winsock operano principalmente sui buffer registrati tramite oggetti **Rio \_ BUFFERID** . Un'applicazione ottiene un **\_ BUFFERID Rio** per un buffer esistente usando la funzione [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) . Un'applicazione può rilasciare una registrazione usando la funzione [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .

Quando un buffer esistente viene registrato come oggetto **Rio \_ BUFFERID** usando la funzione [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , alcune risorse interne vengono allocate dalla memoria fisica e il buffer dell'applicazione esistente verrà bloccato nella memoria fisica. La funzione [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) viene chiamata per annullare la registrazione del buffer, liberare queste risorse interne e consentire il sblocco e il rilascio del buffer dalla memoria fisica.

La registrazione ripetuta e l'annullamento della registrazione dei buffer di applicazione mediante le estensioni I/O registrate di Winsock possono causare un calo significativo delle prestazioni. Quando si progetta un'applicazione utilizzando le estensioni I/O registrate di Winsock, è necessario considerare i seguenti approcci di gestione del buffer per ridurre al minimo la registrazione e l'annullamento della registrazione ripetuti dei buffer dell'applicazione:

-   • Ottimizzare il riutilizzo dei buffer.
-   • Mantenere un pool limitato di buffer registrati non usati per l'uso da parte dell'applicazione.
-   • Mantenere un pool limitato di buffer registrati ed eseguire copie del buffer tra questi buffer registrati e altri buffer non registrati.

Il typedef **Rio \_ BUFFERID** è definito nel file di intestazione *Mswsockdef. h* , che viene incluso automaticamente nel file di intestazione *mswsock. h* . Il file di intestazione *Mswsockdef. h* non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Mswsockdef. h (include mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_BUF Rio**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 
