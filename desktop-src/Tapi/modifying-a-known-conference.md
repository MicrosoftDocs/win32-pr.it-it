---
description: Nel frammento di codice seguente viene illustrata la modifica di un intervallo di tempo di conferenze. L'intervallo di tempo predefinito è 30 minuti. In questo frammento, l'intervallo di tempo è impostato su un anno.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modifica di una conferenza Nota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225861"
---
# <a name="modifying-a-known-conference"></a>Modifica di una conferenza Nota

\[I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Nel frammento di codice seguente viene illustrata la modifica dell'intervallo di tempo di una conferenza. L'intervallo di tempo predefinito è 30 minuti. In questo frammento, l'intervallo di tempo è impostato su un anno.

Questo frammento presuppone che la [connessione a un server ILS](connecting-to-an-ils-server.md) sia già stata eseguita e che sia stata eseguita un' [enumerazione della directory della conferenza](enumerating-conference-directories.md) per ottenere la voce della directory che verrà modificata.

Questo frammento presuppone inoltre che non si tratta di una conferenza multicast. Per modificare gli orari di una conferenza multicast è necessario notificare il server di allocazione indirizzi multicast. Per un esempio di utilizzo dell'indirizzamento multicast, vedere [acquisizione di un indirizzo multicast](acquiring-a-multicast-address.md) .


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



