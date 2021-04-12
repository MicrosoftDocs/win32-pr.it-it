---
title: Il modello di percorso audio sicuro (deprecato)
description: Il modello di percorso audio sicuro (deprecato)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, percorso audio sicuro (SAP)
- Digital Rights Management (DRM), percorso audio sicuro (SAP)
- DRM (Digital Rights Management), Secure Audio Path (SAP)
- Microsoft Secure Audio Path (SAP), modello
- Percorso audio sicuro (SAP), modello
- SAP (percorso audio sicuro), modello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395774"
---
# <a name="the-secure-audio-path-model-deprecated"></a>Il modello di percorso audio sicuro (deprecato)

Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.

Microsoft Secure Audio Path (SAP) è una funzionalità di Microsoft Windows® me e Microsoft Windows XP. Il requisito per la riproduzione di un file audio solo tramite un percorso audio sicuro è specificato nella licenza DRM e viene applicato dai componenti client DRM. Non è stata aggiunta alcuna crittografia aggiuntiva per i file solo SAP quando sono inizialmente protetti. La crittografia SAP viene aggiunta automaticamente dai componenti DRM al momento della riproduzione, così come il processo di autenticazione per tutti i componenti software interessati dalla riproduzione. I lavori di SAP sono quindi completamente trasparenti per le applicazioni e questo è il motivo per cui non esiste alcun metodo o proprietà in Windows Media Format SDK per abilitare o disabilitare SAP. Se lo si desidera, quando si crea un file protetto un proprietario del contenuto può aggiungere un attributo di intestazione personalizzato denominato "DRMHeader. SAPRequired" per indicare a un server licenze di aggiungere il requisito SAP alla licenza. L'implementazione di tale schema è spetta al proprietario del contenuto e al servizio licenze.

Nel modello DRM corrente, se SAP non è applicato, quando viene riprodotta la musica digitale protetta, il contenuto crittografato passa al componente client DRM. Il client DRM verifica che l'applicazione e il componente DRM che incorporano Windows Media Format SDK siano validi. Se sono validi, il client DRM decrittografa il contenuto e lo invia all'applicazione, che quindi lo invia ai componenti audio di livello inferiore. A questo punto, la musica decrittografata è disponibile per le applicazioni in modalità utente e i plug-in e i driver in modalità kernel che possono intercettare i bit audio decrittografati.

Quando viene applicato il requisito del percorso audio protetto, il contenuto non viene decrittografato dall'applicazione, ma viene passato in uno stato crittografato ai componenti di livello inferiore, che sono stati autenticati da Microsoft come affidabili. Un componente audio attendibile è uno che non rende disponibile il contenuto audio per qualsiasi componente di sistema, ad eccezione di altri componenti attendibili specifici. In questo modo, il contenuto digitale rimane protetto fino al livello del driver.

Il diagramma seguente mostra il modello corrente rispetto al modello di percorso audio protetto.

![diagramma del modello di percorso audio sicuro](images/sap.png)

 

 




