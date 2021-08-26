---
description: Specifica un descrittore di buffer registrato utilizzato con le estensioni I/O registrate di Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bde67e14a1cb591922ddc180ab8f308b8429c2b36c5998d313876200cd3a26c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097551"
---
# <a name="rio_bufferid"></a>RIO \_ BUFFERID

Il **typedef RIO \_ BUFFERID** specifica un descrittore di buffer registrato usato con le estensioni di I/O registrate di Winsock.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**RIO \_ BUFFERID**
</dt> <dd>

Tipo di dati che specifica un descrittore di buffer registrato utilizzato con le richieste di invio e ricezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le estensioni di I/O registrate di Winsock operano principalmente sui buffer registrati usando **oggetti \_ BUFFERID RIO.** Un'applicazione ottiene un **\_ BUFFERID RIO** per un buffer esistente usando la [**funzione RIORegisterBuffer.**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) Un'applicazione può rilasciare una registrazione usando la [**funzione RIODeregisterBuffer.**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)

Quando un buffer esistente viene registrato come oggetto **\_ RIO BUFFERID** usando la [**funzione RIORegisterBuffer,**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) alcune risorse interne vengono allocate dalla memoria fisica e il buffer dell'applicazione esistente verrà bloccato nella memoria fisica. La [**funzione RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) viene chiamata per annullare la registrazione del buffer, liberare queste risorse interne e consentire lo sblocco e il rilascio del buffer dalla memoria fisica.

La registrazione ripetuta e la deserializzazione dei buffer dell'applicazione tramite le estensioni di I/O registrate di Winsock possono causare una riduzione significativa delle prestazioni. Quando si progetta un'applicazione usando le estensioni I/O registrate di Winsock per ridurre al minimo la registrazione ripetuta e la deregistrazione dei buffer dell'applicazione, è necessario considerare gli approcci di gestione del buffer seguenti:

-   • Ottimizzare il riutilizzo dei buffer.
-   • Mantenere un pool limitato di buffer registrati inutilizzati per l'uso da parte dell'applicazione.
-   • Mantenere un pool limitato di buffer registrati ed eseguire copie del buffer tra questi buffer registrati e altri buffer non registrati.

Il **typedef RIO \_ BUFFERID** è definito nel file di intestazione *Mswsockdef.h* che viene automaticamente incluso nel file di intestazione *Mswsock.h.* Il file *di intestazione Mswsockdef.h* non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Mswsockdef.h (includere Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RIO \_ BUF**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**RIOSEND**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 
