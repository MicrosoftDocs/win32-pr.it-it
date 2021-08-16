---
description: Per usare i certificati per la sicurezza, è necessario verificare l'autenticità e la validità di ogni certificato ricevuto. Questa verifica dipende dal concetto di attendibilità e dalla delega di attendibilità \[ di Platform Software Development Kit (SDK). \]
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Catene di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6efdd49cbd66c74805cc560286e5f15a981ef200df5523c602c2bb4b395a04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771940"
---
# <a name="certificate-chains"></a>Catene di certificati

Per usare [*i certificati*](../secgloss/c-gly.md) per la sicurezza, è necessario verificare l'autenticità e la validità di ogni certificato ricevuto. Questa verifica dipende dal concetto di attendibilità e dalla delega del trust. Per altre informazioni, vedere [Gerarchia di attendibilità](hierarchy-of-trust.md).

Ogni certificato contiene un campo oggetto che identifica l'utente o il gruppo a cui è stato emesso il certificato. Ogni certificato contiene anche un campo autorità di certificazione che identifica l'autorità [*di*](../secgloss/c-gly.md) certificazione (CA) in grado di certificare l'identità del soggetto.

Una catena di certificati è costituita da tutti i certificati necessari per certificare il soggetto identificato dal certificato finale. In pratica questo include il certificato finale, i certificati delle CA intermedie e il certificato di una CA radice considerato attendibile da tutte le parti della catena. Ogni CA intermedia nella catena contiene un certificato emesso dalla CA a un livello superiore nella gerarchia di attendibilità. La CA radice emissione di un certificato per se stessa.

Il processo di verifica dell'autenticità e della validità di un certificato appena ricevuto comporta il controllo di tutti i certificati nella catena di certificati della CA originale, universalmente attendibile, tramite qualsiasi AUTORITÀ di certificazione intermedia, fino al certificato appena ricevuto, denominato certificato finale. Un nuovo certificato può essere considerato attendibile solo se ogni certificato nella catena del certificato viene emesso correttamente e valido.

Tenere traccia di tutti i certificati che ese backup di un nuovo certificato finale può diventare complicato. Pertanto, [*la tecnologia CryptoAPI*](../secgloss/c-gly.md) 2.0 offre funzioni che automatizzano la creazione della catena di certificati che esere back qualsiasi certificato finale specificato. Queste funzioni controllano e segnalano anche la validità di ogni certificato in una catena.

Le funzioni di creazione e controllo della catena [*di CryptoAPI*](../secgloss/c-gly.md) 2.0 usano un motore a catena per creare e verificare catene di certificati. Un motore di catena definisce uno spazio dei nomi dell'archivio e il partizionamento della cache per l'infrastruttura di concatenamento dei certificati. CryptoAPI 2.0 un motore a catena predefinito per qualsiasi processo dell'applicazione che usa solo archivi di sistema predefiniti ,ad esempio MY, Root, CA e Trust, per la compilazione e la memorizzazione nella cache della catena. Un'applicazione può definire il proprio spazio dei nomi dell'archivio o avere una propria cache partizionata creando il proprio motore di catena. Per ottenere un comportamento ottimale per la memorizzazione nella cache, è consigliabile creare un motore a catena singola all'avvio dell'applicazione e usarlo per tutta la durata dell'applicazione.

Per un elenco di funzioni, vedere [Funzioni di verifica della catena di certificati](cryptography-functions.md). Per un programma che compila catene di certificati e verifica i certificati, vedere [Esempio di programma C: Creazione di una catena di certificati](example-c-program-creating-a-certificate-chain.md).

 

 
