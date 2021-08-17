---
title: Componente kernel DRM (deprecato)
description: Componente kernel DRM (deprecato)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- digital rights management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management),Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, Secure Audio Path (SAP)
- Digital Rights Management (DRM), Secure Audio Path (SAP)
- DRM (Digital Rights Management),Secure Audio Path (SAP)
- Windows Media Format SDK, componente kernel DRM
- DRM (Digital Rights Management), componente kernel
- DRM (Digital Rights Management),componente kernel
- Microsoft Secure Audio Path (SAP),componente kernel DRM
- Secure Audio Path (SAP),componente kernel DRM
- SAP (Secure Audio Path),componente kernel DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8db4389d9156ef13d9e87983a4ae433e6028805268f3cbd55690d4d0d8144b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845758"
---
# <a name="the-drm-kernel-component-deprecated"></a>Componente kernel DRM (deprecato)

Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.

Nel modello Microsoft Secure Audio Path (SAP), il componente kernel DRM offre due funzionalità di base che proteggono l'integrità della musica crittografata.

In primo luogo, il componente client DRM e il componente kernel DRM sono in comunicazione quando viene riprodotto un file musicale. Questa comunicazione tra componenti impedisce a chiunque di manomettere il segnale crittografato o di inserire informazioni false.

In secondo momento, il componente kernel DRM non decrittografa il segnale musicale fino a quando tutti i componenti rimanenti non vengono autenticati. Ovvero, prima di decrittografare il contenuto e passarlo al componente di sistema successivo, il componente kernel DRM controlla ogni componente che rimane nel percorso della scheda audio (ogni componente che può accedere al contenuto) e verifica che questi componenti siano firmati con un certificato di Microsoft. Un componente non firmato potrebbe indicare un componente sospetto o un driver dannoso. Pertanto, quando il componente del kernel DRM convalida i componenti rimanenti, se un componente non supera questo test, il segnale viene interrotto e non può essere riprodotto. In caso contrario, se tutti i componenti superano la convalida, il componente kernel DRM decrittografa la musica e la passa al componente successivo.

Microsoft firma digitalmente i driver che superano Windows® test WHQL (Hardware Quality Lab) per garantire agli utenti che usano i driver di massima qualità. Questa procedura è standard e garantisce l'autenticità dei componenti perché la firma non può essere contraffatta, né il codice può essere modificato senza eliminare la firma. I driver certificati per Secure Audio Path devono proteggere i dati audio che elaborano dall'accesso da parte di componenti non attendibili. 

I driver inclusi in Windows Millennium Edition e Windows XP vengono aggiornati per Secure Audio Path e firmati. I driver non firmati per l'uso con Windows Me o Windows XP non possono riprodurre musica protetta. I produttori di driver possono riemettere versioni aggiornate dei driver firmati da WHQL e pubblicarle su Internet per il download da parte degli utenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Percorso audio sicuro Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




