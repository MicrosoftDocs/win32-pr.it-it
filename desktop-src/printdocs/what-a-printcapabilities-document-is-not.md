---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Cosa non è un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320984"
---
# <a name="what-a-printcapabilities-document-is-not"></a>Cosa non è un documento PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

È utile elencare alcune funzionalità e informazioni che il documento PrintCapabilities non è destinato a fornire.

Documento PrintCapabilities:

-   Non rappresenta dati multivalore (dipendenti dalla configurazione).

    Ogni documento PrintCapabilities viene costruito per una configurazione specifica. Nessuna proprietà o ScoredProperty nel documento può avere un valore che dipende dalla configurazione specifica. Nella versione iniziale dello schema, il provider PrintCapabilities deve elaborare l'oggetto PrintTicket di input e creare un documento PrintCapabilities che contiene i valori delle proprietà appropriati per la configurazione specificata nell'oggetto PrintTicket.

-   Non contiene informazioni sui vincoli.

    Il documento PrintCapabilities non indica quali configurazioni sono consentite e quali non sono consentite. Nella versione iniziale dello schema, il provider PrintCapabilities deve archiviare tutte le informazioni necessarie per convalidare le configurazioni, fornire un metodo che convalida l'oggetto PrintTicket di input e restituire un oggetto PrintTicket corretto nel caso in cui l'oggetto PrintTicket specificato violi uno o più vincoli.

-   Non contiene informazioni dinamiche sul dispositivo.

    Si è verificato un sovraccarico eccessivo nella costruzione del documento PrintCapabilities affinché venga utilizzato per mantenere le informazioni sullo stato in rapida evoluzione, ad esempio i livelli di input penna, la carta rimanente in ogni barra o lo stato di inceppamento della carta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



