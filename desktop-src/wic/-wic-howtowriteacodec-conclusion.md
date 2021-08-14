---
description: La compilazione del codec nella piattaforma wic (Windows Imaging Component) consente a tutte le applicazioni create su WIC di ottenere lo stesso supporto della piattaforma per il formato di immagine che ottengono per i formati di immagine comuni forniti con la piattaforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusione (Come scrivere un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5288438ea518e1776562b288184067df6d82c326eb6786b163f20e90c6febc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205822"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Conclusione (Come scrivere un codec WIC-Enabled)

La compilazione del codec nella piattaforma wic (Windows Imaging Component) consente a tutte le applicazioni create su WIC di ottenere lo stesso supporto della piattaforma per il formato di immagine che ottengono per i formati di immagine comuni forniti con la piattaforma. Consente inoltre a Windows Vista Raccolta foto, Windows Explorer e Visualizzatore foto di visualizzare le anteprime e le anteprime delle immagini nel formato usando il decodificatore fornito. Per i formati non elaborati, consente alle applicazioni di creazione di immagini più sofisticate di sfruttare le funzionalità di elaborazione non elaborata del decodificatore. A seconda delle opzioni del codificatore supportate, è anche possibile esporre funzionalità univoche del codificatore per consentire alle applicazioni di sfruttare al meglio le funzionalità avanzate del formato immagine.

Lo sviluppo di un codec abilitato per WIC richiede l'implementazione di alcune nuove interfacce. In molti casi, è possibile scrivere un wrapper per il codec esistente che implementa queste interfacce. Quando si installa il codec, è necessario creare alcune voci del Registro di sistema per rendere il codec individuabile dalla piattaforma WIC e associarlo ai gestori di metadati appropriati. È anche necessario richiamare un'API per cancellare la cache delle anteprime predefinite (vuote) che potrebbero essere state precedentemente associate alle immagini nel formato. Se si vuole, è possibile abilitare il Windows Vista Raccolta foto per fornire agli utenti un collegamento per scaricare il codec quando il Raccolta foto rileva un'immagine con l'estensione del nome file. A tale scopo, è necessario fornire a Microsoft informazioni sull'estensione del nome file del codec e sull'URL per il sito di download.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Installazione e registrazione codec](-wic-codecinstallandreg.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



