---
title: Modello di percorso audio sicuro (deprecato)
description: Modello di percorso audio sicuro (deprecato)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- digital rights management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management),Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, Secure Audio Path (SAP)
- Digital Rights Management (DRM), Secure Audio Path (SAP)
- DRM (Digital Rights Management),Secure Audio Path (SAP)
- Microsoft Secure Audio Path (SAP),model
- Percorso audio sicuro (SAP), modello
- SAP (Secure Audio Path),model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a381d29bcbf4b09ae989325cd5b35c332a6f316c1f932868437ac93a7854ab58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084287"
---
# <a name="the-secure-audio-path-model-deprecated"></a>Modello di percorso audio sicuro (deprecato)

Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.

Microsoft Secure Audio Path (SAP) è una funzionalità di Microsoft Windows® Me e Microsoft Windows XP. Il requisito che un file audio deve essere riprodotto solo tramite un percorso audio sicuro è specificato nella licenza DRM e applicato dai componenti client DRM. Non è stata aggiunta alcuna crittografia aggiuntiva per i file solo SAP quando sono inizialmente protetti. La crittografia SAP viene aggiunta automaticamente dai componenti DRM in fase di riproduzione, così come il processo di autenticazione per tutti i componenti software coinvolti nella riproduzione. Il funzionamento di SAP è quindi completamente trasparente per le applicazioni ed è per questo motivo che non è disponibile alcun metodo o proprietà in Windows Media Format SDK per l'abilitazione o la disabilitazione di SAP. Se si desidera, quando si crea un file protetto, un proprietario del contenuto può aggiungere un attributo di intestazione personalizzato denominato simile a "DRMHeader.SAPRequired" per indicare a un server licenze di aggiungere il requisito SAP alla licenza. L'implementazione di tale schema è a servizio del proprietario del contenuto e del servizio licenze.

Nel modello DRM corrente, se SAP non viene applicato, quando viene riprodotta musica digitale protetta, il contenuto crittografato passa al componente client DRM. Il client DRM verifica che l'applicazione e il componente DRM che incorpora il Windows Media Format SDK siano validi. Se sono validi, il client DRM decrittografa il contenuto e lo invia all'applicazione, che lo invia ai componenti audio di livello inferiore. A questo punto, la musica decrittografata è disponibile per le applicazioni in modalità utente e i plug-in e i driver in modalità kernel in grado di intercettare i bit audio decrittografati.

Quando viene applicato il requisito secure audio path, il contenuto non viene decrittografato dall'applicazione, ma viene passato in uno stato crittografato ai componenti di livello inferiore, tutti autenticati da Microsoft come attendibili. Un componente audio attendibile è un componente che non rende disponibile il contenuto audio per alcun componente di sistema ad eccezione di altri componenti attendibili specifici. In questo modo, il contenuto digitale rimane protetto fino al livello del driver.

Nel diagramma seguente viene visualizzato il modello corrente rispetto al modello Secure Audio Path.

![diagramma del modello di percorso audio sicuro](images/sap.png)

 

 




