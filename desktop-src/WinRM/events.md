---
title: Eventi (Gestione remota Windows)
description: Il servizio raccolta eventi utilizza il protocollo WS-Management per raccogliere gli eventi da computer remoti.
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06f96877904a5e76ea61a6b2f636e962e4dbd9b9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400076"
---
# <a name="events-windows-remote-management"></a>Eventi (Gestione remota Windows)

Il servizio raccolta eventi utilizza il protocollo WS-Management per raccogliere gli eventi da computer remoti. Con il servizio raccolta eventi è possibile creare sottoscrizioni a eventi di Windows su computer remoti e eventi hardware generati da BMC (battiscopa Management Controllers). BMC deve supportare il protocollo WS-Management.

Quando si crea una sottoscrizione, gli eventi vengono trasmessi al computer in cui è stata creata la sottoscrizione. Verranno visualizzati nel Visualizzatore eventi.

Gli eventi hardware generati da Intelligent Platform Management Interface (IPMI) nei computer basati su Windows vengono raccolti localmente usando il driver IPMI e archiviati nel registro eventi hardware, dopo i quali possono essere trasmessi come altri eventi del sistema operativo Windows.

È possibile creare sottoscrizioni utilizzando lo strumento da riga di comando Wecutil.exe. Per ulteriori informazioni sull'utilizzo di questo strumento, digitare **wecutil/?** al prompt dei comandi. Per ulteriori informazioni sul servizio raccolta eventi, vedere [raccolta di eventi di Windows](/windows/desktop/WEC/windows-event-collector).

> [!Note]  
> Gestione remota Windows API richiedono che tutti gli indirizzi IPv6 siano racchiusi tra parentesi quadre.

 

> [!Caution]
>
> Quando si utilizzano le sottoscrizioni avviate da agente di raccolta, limitare il numero di computer remoti a 500 e isolare il servizio [raccolta eventi Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) in un processo host separato.
>
> Un errore di connessione conterrà un thread finché non si verifica il timeout. Un numero elevato di errori di connessione simultanei può causare l'esaurimento del pool di thread e il rendering del server che non risponde.

 

 

 
