---
description: Per utilizzare i certificati per la sicurezza, è necessario verificare l'autenticità e la validità di ogni certificato ricevuto. Questa verifica dipende dal concetto di attendibilità e dalla delega del \[ Software Development Kit (SDK) della piattaforma di attendibilità \] .
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Catene di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea42b6788997a86aade6f89d0f35d92a74daafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484692"
---
# <a name="certificate-chains"></a>Catene di certificati

Per utilizzare i [*certificati*](../secgloss/c-gly.md) per la sicurezza, è necessario verificare l'autenticità e la validità di ogni certificato ricevuto. Questa verifica dipende dal concetto di attendibilità e dalla delega del trust; Per ulteriori informazioni, vedere [gerarchia di trust](hierarchy-of-trust.md).

Ogni certificato contiene un campo oggetto che identifica il singolo o il gruppo a cui è stato emesso il certificato. Ogni certificato contiene anche un campo emittente che identifica l' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) autorizzata a certificare l'identità dell'oggetto.

Una catena di certificati è costituita da tutti i certificati necessari per certificare il soggetto identificato dal certificato finale. In pratica, include il certificato finale, i certificati delle autorità di certificazione intermedie e il certificato di una CA radice considerata attendibile da tutte le parti della catena. Ogni CA intermedia nella catena include un certificato emesso dalla CA un livello al di sopra di esso nella gerarchia di trust. La CA radice rilascia un certificato per se stesso.

Il processo di verifica dell'autenticità e della validità di un certificato appena ricevuto prevede il controllo di tutti i certificati nella catena di certificati dalla CA originale, universalmente attendibile, attraverso qualsiasi CA intermedia, fino al certificato appena ricevuto, denominato certificato finale. Un nuovo certificato può essere considerato attendibile solo se ogni certificato nella catena del certificato viene emesso correttamente e valido.

Il rilevamento di tutti i certificati che restituiscono un nuovo certificato finale può diventare complesso. Quindi, la tecnologia [*CryptoAPI*](../secgloss/c-gly.md) 2,0 fornisce funzioni che automatizzano la creazione della catena di certificati che eseguono il backup di qualsiasi certificato finale. Queste funzioni controllano e segnalano anche la validità di ogni certificato in una catena.

Le funzioni di creazione e controllo della catena di [*CryptoAPI*](../secgloss/c-gly.md) 2,0 usano un motore a catena per creare e verificare catene di certificati. Un motore a catena definisce uno spazio dei nomi dell'archivio e il partizionamento della cache per l'infrastruttura di concatenamento dei certificati. CryptoAPI 2.0 fornisce un motore a catena predefinito per qualsiasi processo dell'applicazione che usa solo archivi di sistema predefiniti (ad esempio, MY, root, CA e trust) per la compilazione e la memorizzazione nella cache della catena. Un'applicazione può definire il proprio spazio dei nomi dell'archivio o la propria cache partizionata creando il proprio motore a catena. Per ottenere un comportamento ottimale della memorizzazione nella cache, è consigliabile creare un motore a catena singolo all'avvio dell'applicazione e usare tale motore a catena per tutta la durata dell'applicazione.

Per un elenco di funzioni, vedere [funzioni di verifica della catena di certificati](cryptography-functions.md). Per un programma che compila catene di certificati e verifica i certificati, vedere [esempio C programma: creazione di una catena di certificati](example-c-program-creating-a-certificate-chain.md).

 

 
