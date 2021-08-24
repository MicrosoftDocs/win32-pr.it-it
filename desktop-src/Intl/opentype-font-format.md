---
description: Il formato del tipo di carattere OpenType basato su Unicode estende il formato di file del tipo di carattere TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato dei tipi di carattere OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18324f3a9c84553da81c9f9723a2ecd67c03539b4dd39c7a80afc4be5cdcda66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147094"
---
# <a name="opentype-font-format"></a>Formato dei tipi di carattere OpenType

Il formato del tipo di carattere OpenType basato su Unicode estende il formato di file del tipo di carattere TrueType. I tipi di carattere OpenType consentono il mapping tra caratteri e [glifi,](uniscribe-glossary.md)abilitando il supporto per legature, forme posizionali, alternative e altre sostituzioni. I tipi di carattere OpenType possono anche includere informazioni che supportano il posizionamento bidimensionale dei glifi e l'allegato del glifo e possono contenere strutture TrueType o PostScript struttura.

Le funzionalità di layout all'interno dei tipi di carattere OpenType sono organizzate in base a script e linguaggi, consentendo a un singolo tipo di carattere di supportare più sistemi di scrittura, anche all'interno dello stesso script. Per garantire la coerenza nelle operazioni di layout del testo ed evitare un sovraccarico non necessario nei file o nelle applicazioni dei tipi di carattere, molti degli algoritmi di layout del testo e della semantica della lingua sono inclusi in Uniscribe. In questo modo lo sviluppatore di tipi di carattere non deve definire regole di script generalizzate all'interno di un tipo di carattere.

Le applicazioni possono introdurre specifiche conoscenze o preferenze relative al layout dello script. I tipi di carattere di layout OpenType possono anche contenere regole di layout che duplicano o sorrendono quelle applicate dai servizi del sistema operativo. La struttura a più livelli dei servizi del sistema operativo che supportano il layout del testo consente a un'applicazione di scegliere le informazioni sul layout da usare e di selezionare come applicarlo. Per altre informazioni, vedere la [panoramica delle specifiche tipografiche Microsoft](https://www.microsoft.com/typography/SpecificationsOverview.mspx) o la specifica [OpenType.](https://www.microsoft.com/typography/otspec/)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



