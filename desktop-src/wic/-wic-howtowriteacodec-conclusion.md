---
description: La creazione di un codec sulla piattaforma Windows Imaging Component (WIC) consente a tutte le applicazioni basate su WIC di ottenere lo stesso supporto di piattaforma per il formato di immagine ottenuto per i formati di immagine comuni forniti con la piattaforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusione (come scrivere un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312976"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Conclusione (come scrivere un codec WIC-Enabled)

La creazione di un codec sulla piattaforma Windows Imaging Component (WIC) consente a tutte le applicazioni basate su WIC di ottenere lo stesso supporto di piattaforma per il formato di immagine ottenuto per i formati di immagine comuni forniti con la piattaforma. Consente inoltre la raccolta foto di Windows Vista, Esplora risorse e Visualizzatore foto per visualizzare anteprime e anteprime delle immagini nel formato usando il decodificatore fornito. Per i formati RAW, consente alle applicazioni di imaging più sofisticate di sfruttare le funzionalità di elaborazione non elaborate del decodificatore. A seconda delle opzioni del codificatore supportate, è anche possibile esporre funzionalità univoche del codificatore per consentire alle applicazioni di sfruttare al meglio le funzionalità avanzate del formato di immagine.

Per lo sviluppo di un codec abilitato per WIC è necessario implementare alcune nuove interfacce. In molti casi, è possibile scrivere un wrapper per il codec esistente che implementa tali interfacce. Quando si installa il codec, è necessario apportare alcune voci del registro di sistema per rendere individuabile il codec dalla piattaforma WIC e associarlo ai gestori di metadati appropriati. È anche necessario richiamare un'API per cancellare la cache delle anteprime delle anteprime predefinite (vuote) che potrebbero essere state precedentemente associate alle immagini nel formato. Se lo si desidera, è possibile abilitare la raccolta foto di Windows Vista per fornire agli utenti un collegamento per scaricare il codec quando la raccolta foto rileva un'immagine con l'estensione del nome file. A tale scopo, è necessario fornire a Microsoft informazioni sull'estensione del nome file del codec e sull'URL per il sito di download.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Installazione e registrazione di CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



