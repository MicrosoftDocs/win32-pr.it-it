---
description: Informazioni su alcune funzionalità e informazioni che il documento PrintCapabilities non è destinato a fornire.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Cosa non è un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409894"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Cosa non è un documento PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

È opportuno elencare alcune delle funzionalità e delle informazioni che il documento PrintCapabilities non è destinato a fornire.

Un documento PrintCapabilities:

-   Non rappresenta dati multivalore (dipendenti dalla configurazione).

    Ogni documento PrintCapabilities viene costruito per una configurazione specifica. Nessuna proprietà o ScoredProperty nel documento può avere un valore che dipende dalla configurazione specifica. Nella versione dello schema iniziale, il provider PrintCapabilities deve elaborare l'input PrintTicket e creare un documento PrintCapabilities contenente i valori property appropriati per la configurazione specificata in PrintTicket.

-   Non contiene informazioni sui vincoli.

    Il documento PrintCapabilities non indica quali configurazioni sono consentite e quali non sono consentite. Nella versione iniziale dello schema, il provider PrintCapabilities deve archiviare le informazioni necessarie per convalidare le configurazioni, fornire un metodo che convalida l'input PrintTicket e restituire un PrintTicket corretto nel caso in cui il PrintTicket specificato violi uno o più vincoli.

-   Non contiene informazioni dinamiche sul dispositivo.

    La creazione del documento PrintCapabilities comporta un sovraccarico troppo alto per poter essere usato per contenere informazioni sullo stato in rapida evoluzione, ad esempio i livelli di input penna, la carta rimanente in ogni vassoio lo stato di inceppamento della carta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



