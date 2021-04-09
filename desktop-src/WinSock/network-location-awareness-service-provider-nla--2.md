---
description: I personal computer che eseguono Microsoft Windows hanno spesso numerose connessioni di rete, ad esempio più schede di interfaccia di rete (NIC) connesse a reti diverse o una connessione di rete fisica e una connessione remota.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Provider del servizio di riconoscimento del percorso di rete (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129143"
---
# <a name="network-location-awareness-service-provider-nla"></a>Provider del servizio di riconoscimento del percorso di rete (NLA)

I personal computer che eseguono Microsoft Windows hanno spesso numerose connessioni di rete, ad esempio più schede di interfaccia di rete (NIC) connesse a reti diverse o una connessione di rete fisica e una connessione remota. Windows Sockets è stato in grado di enumerare le interfacce di rete disponibili per un certo periodo di tempo, ma alcune informazioni critiche sulle connessioni di rete non erano disponibili in precedenza. Sono incluse informazioni quali la rete logica a cui è collegato un computer Windows o se più interfacce sono connesse alla stessa rete.

Il provider del servizio di riconoscimento del percorso di rete, comunemente noto come NLA, consente alle applicazioni Windows Sockets 2 di identificare la rete logica a cui è collegato un computer Windows. Inoltre, NLA consente alle applicazioni Windows Sockets di identificare l'interfaccia di rete fisica che una determinata applicazione ha salvato informazioni specifiche. NLA viene implementato come provider di servizi di risoluzione dei nomi Windows Sockets 2 generico.

 

 



