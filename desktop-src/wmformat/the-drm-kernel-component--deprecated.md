---
title: Componente kernel DRM (deprecato)
description: Componente kernel DRM (deprecato)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, percorso audio sicuro (SAP)
- Digital Rights Management (DRM), percorso audio sicuro (SAP)
- DRM (Digital Rights Management), Secure Audio Path (SAP)
- Windows Media Format SDK, componente kernel DRM
- Digital Rights Management (DRM), componente kernel
- DRM (Digital Rights Management), componente kernel
- Microsoft Secure Audio Path (SAP), componente kernel DRM
- Secure Audio Path (SAP), componente kernel DRM
- SAP (Secure Audio Path), componente kernel DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047576"
---
# <a name="the-drm-kernel-component-deprecated"></a>Componente kernel DRM (deprecato)

Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.

Nel modello Microsoft Secure Audio Path (SAP) il componente kernel DRM fornisce due funzionalità di base che proteggono l'integrità della musica crittografata.

In primo luogo, il componente client DRM e il componente kernel DRM sono in comunicazione quando viene riprodotto un file musicale. Questa comunicazione tra i componenti impedisce a chiunque di manomettere il segnale crittografato o di inserire informazioni false.

In secondo luogo, il componente kernel DRM non decrittografa il segnale musicale finché non vengono autenticati tutti i componenti rimanenti. Ovvero, prima di decrittografare il contenuto e passarlo al componente di sistema successivo, il componente kernel DRM controlla ogni componente che rimane nel percorso alla scheda audio (ogni componente che può accedere al contenuto) e verifica che questi componenti siano firmati con un certificato di Microsoft. Un componente non firmato potrebbe indicare un componente sospetto o un driver dannoso. Pertanto, quando il componente kernel DRM convalida i componenti rimanenti, se il test ha esito negativo, il segnale viene interrotto e non può essere riprodotto. In caso contrario, se tutti i componenti passano la convalida, il componente kernel DRM decrittografa la musica e la passa al componente successivo.

Microsoft firma digitalmente i driver che passano i test Windows® Hardware Quality Lab (WHQL) per garantire agli utenti che utilizzano i driver di qualità più elevata. Questa pratica è standard e garantisce l'autenticità dei componenti perché la firma non può essere falsificata, né può essere modificata senza eliminare definitivamente la firma. I driver certificati per il percorso audio sicuro devono proteggere i dati audio che elaborano dall'accesso da parte di componenti non attendibili. 

I driver inclusi in Windows Millennium Edition e Windows XP vengono aggiornati per il percorso audio protetto e firmati. I driver non firmati per l'utilizzo con Windows me o Windows XP non possono riprodurre musica protetta. I produttori di driver possono riemettere le versioni aggiornate dei driver firmati da WHQL e pubblicarli in Internet per il download da parte degli utenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Percorso audio protetto Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




