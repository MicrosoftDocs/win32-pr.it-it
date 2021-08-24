---
description: Il frammento di codice seguente illustra la modifica di un intervallo di tempo delle conferenze. L'intervallo di tempo predefinito è di 30 minuti. In questo frammento, l'intervallo di tempo è impostato su un anno.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modifica di una conferenza nota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b139b05f70f801a28b91ecb6c2773fd740f10df7c0fd2b8e86b904b210cc50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575601"
---
# <a name="modifying-a-known-conference"></a>Modifica di una conferenza nota

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il frammento di codice seguente illustra la modifica dell'intervallo di tempo di una conferenza. L'intervallo di tempo predefinito è di 30 minuti. In questo frammento, l'intervallo di tempo è impostato su un anno.

Questo frammento presuppone che sia già stata eseguita la connessione a un [server ILS](connecting-to-an-ils-server.md) e che sia stata eseguita un'enumerazione della [directory](enumerating-conference-directories.md) delle conferenze per ottenere la voce di directory che verrà modificata.

Questo frammento presuppone anche che non si tratta di una conferenza multicast. La modifica degli orari di una conferenza multicast richiede la notifica del server di allocazione degli indirizzi multicast. Per [un esempio di utilizzo dell'indirizzamento multicast,](acquiring-a-multicast-address.md) vedere Acquisizione di un indirizzo multicast.


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



