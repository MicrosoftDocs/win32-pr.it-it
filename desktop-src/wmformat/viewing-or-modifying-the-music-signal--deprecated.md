---
title: Visualizzazione o modifica del segnale musicale (deprecato)
description: Visualizzazione o modifica del segnale musicale (deprecato)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, percorso audio sicuro (SAP)
- Digital Rights Management (DRM), percorso audio sicuro (SAP)
- DRM (Digital Rights Management), Secure Audio Path (SAP)
- Windows Media Format SDK, visualizzazione o modifica di segnali musicali
- Digital Rights Management (DRM), visualizzazione o modifica di segnali musicali
- DRM (Digital Rights Management), visualizzazione o modifica di segnali musicali
- Microsoft Secure Audio Path (SAP), Music Signal Viewing o Modifying
- Percorso audio sicuro (SAP), visualizzazione o modifica di segnali musicali
- SAP (percorso audio sicuro), visualizzazione o modifica di segnali musicali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298823"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a>Visualizzazione o modifica del segnale musicale (deprecato)

Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.

Nel modello Microsoft Secure Audio Path (SAP), le applicazioni non possono modificare la musica protetta in alcun modo. Ad esempio, quando un'applicazione tenta di intercettare un segnale musicale, il segnale suona come un rumore casuale. Di conseguenza, le applicazioni che in genere modificano i segnali, ad esempio un equalizzatore, non possono modificare il suono della musica.

Alcune applicazioni visualizzano semplicemente un segnale musicale. Alcune applicazioni, ad esempio, visualizzano le spie lampeggianti nel tempo con il segnale musicale, ma non la modifica. Per supportare le applicazioni che visualizzano i segnali, una piccola parte della musica viene decrittografata e passata in formato chiaro con il contenuto crittografato. Il segnale risultante è molto scarso (peggio la qualità del telefono) ma può essere sufficiente per le applicazioni che visualizzano i segnali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Percorso audio protetto Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




