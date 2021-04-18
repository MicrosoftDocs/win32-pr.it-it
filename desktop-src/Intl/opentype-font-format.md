---
description: Il formato del tipo di carattere OpenType basato su Unicode estende il formato del file del tipo di carattere TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato dei tipi di carattere OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319053"
---
# <a name="opentype-font-format"></a>Formato dei tipi di carattere OpenType

Il formato del tipo di carattere OpenType basato su Unicode estende il formato del file del tipo di carattere TrueType. I tipi di carattere OpenType consentono il mapping tra caratteri e [glifi](uniscribe-glossary.md), abilitando il supporto per legature, moduli posizionali, alternative e altre sostituzioni. I tipi di carattere OpenType possono includere anche informazioni che supportano il posizionamento del glifo bidimensionale e l'allegato del glifo e possono contenere strutture TrueType o PostScript.

Le funzionalità di layout nei tipi di carattere OpenType sono organizzate in base a script e linguaggi, consentendo a un singolo tipo di carattere di supportare più sistemi di scrittura, anche nello stesso script. Per garantire la coerenza nelle operazioni di layout del testo ed evitare un sovraccarico superfluo nei file o nelle applicazioni dei tipi di carattere, molti degli algoritmi di layout del testo e semantica del linguaggio sono inclusi in Uniscribe. Ciò consente allo sviluppatore di tipi di carattere di definire regole di script generalizzate all'interno di un tipo di carattere.

Le applicazioni possono introdurre conoscenze specifiche o preferenze relative al layout di script. I tipi di carattere del layout OpenType potrebbero contenere anche regole di layout che duplicano o sostituiscono quelle applicate dai servizi del sistema operativo. La struttura a più livelli dei servizi del sistema operativo che supportano il layout del testo consente a un'applicazione di scegliere le informazioni sul layout da usare e di selezionare la modalità di applicazione. Per ulteriori informazioni, vedere [Cenni preliminari sulle specifiche di Microsoft Typography](https://www.microsoft.com/typography/SpecificationsOverview.mspx) o la [specifica OpenType](https://www.microsoft.com/typography/otspec/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



