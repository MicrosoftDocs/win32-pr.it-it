---
description: L'agente DDE di rete avvia la rete DDE se rileva l'attività DDE della rete locale.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agente DDE di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305708"
---
# <a name="network-dde-agent"></a>Agente DDE di rete

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

L'agente DDE di rete avvia la rete DDE se rileva l'attività DDE della rete locale. Non rileva un client remoto che tenta di connettersi. Pertanto, prima che un client possa connettersi correttamente, è necessario avviare la rete DDE sul computer server. Si noti che la rete DDE non è avviata per impostazione predefinita. Per avviare la rete DDE, eseguire NETDDE.EXE. Questo file si trova nella directory di Windows.

L'agente DDE di rete avvia anche le applicazioni necessarie per la rete DDE. Una volta avviata la rete DDE, le conversazioni DDE vengono controllate tramite una finestra DDE di rete associata a una delle applicazioni DDE di rete. Questa applicazione funge da proxy. Comunica con tutte le applicazioni DDE locali e remote.

 

 



