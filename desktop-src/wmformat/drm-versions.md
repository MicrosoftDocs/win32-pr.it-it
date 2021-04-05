---
title: Versioni DRM
description: Versioni DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media Format SDK, versioni DRM
- Digital Rights Management (DRM), versioni
- DRM (Digital Rights Management), versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955327"
---
# <a name="drm-versions"></a>Versioni DRM

Sono disponibili diverse versioni di Windows Media Digital Rights Management (DRM). La versione 1 di DRM è spesso impostata separatamente dalle altre versioni di questa documentazione, perché viene implementata usando tecniche diverse dalle versioni successive. La seconda generazione di Windows Media DRM è denominata DRM versione 7 perché è stata introdotta come parte di Windows Media Format 7 SDK. Viene talvolta definito DRM versione 2. Le versioni successive di Windows Media DRM, DRM versione 9 e il nuovo Windows Media DRM 10 sono estensioni di DRM versione 7 e utilizzano le stesse procedure per l'implementazione. Tutte le versioni di Windows Media DRM utilizzano le stesse routine di crittografia; le differenze tra le versioni riguardano le funzionalità delle licenze.

Quando si creano file protetti usando gli oggetti di Windows Media Format SDK, è necessario supportare sia la versione 1 che la versione più recente. I file protetti da DRM versione 1 sono diversi da quelli protetti da versioni successive solo nel contenuto dell'intestazione. I file più recenti contenenti le informazioni aggiuntive sull'intestazione possono comunque essere usati nei client che eseguono il rendering solo del contenuto della versione 1. Sebbene le versioni successive di DRM offrano un livello più elevato di sicurezza e funzionalità aggiuntive, esistono ancora molti giocatori che usano solo la versione 1.

Per ulteriori informazioni sulle versioni DRM, vedere la documentazione di Windows Media Rights Manager SDK.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




