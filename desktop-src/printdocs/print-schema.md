---
description: Questa panoramica descrive lo schema di stampa e i collegamenti agli argomenti di riferimento sullo schema di stampa. Lo schema di stampa include le parole chiave dello schema di stampa e il framework.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Riferimento allo schema di stampa legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407134"
---
# <a name="legacy-print-schema-reference"></a>Riferimento allo schema di stampa legacy

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa e le tecnologie correlate sono disponibili in Microsoft .NET Framework 3.0, Microsoft Windows Vista e versioni successive.

Lo schema di stampa fornisce un formato basato su XML per esprimere e organizzare un ampio set di proprietà che descrivono un formato di processo o PrintCapabilities in modo strutturato gerarchicamente.

Lo schema di stampa è un termine generico che include due componenti, Print Schema Keywords e Print Schema Framework. Il documento Print Schema Keywords (Parole chiave dello schema di stampa) è uno schema pubblico che definisce un set di istanze di elementi che possono essere usate per descrivere gli attributi del dispositivo e la formattazione del processo di stampa. Print Schema Framework è uno schema pubblico che definisce una raccolta strutturata gerarchicamente di tipi di elementi XML e specifica come i tipi di elemento possono essere usati insieme.

Le parole chiave dello schema di stampa e il framework dello schema di stampa sono alla base di due tecnologie correlate allo schema di stampa, lo schema PrintCapabilities e lo schema PrintTicket.

È importante tenere presente che uno degli obiettivi dello schema di stampa è il supporto delle estensioni dello schema da parte dei provider. Ciò significa che i provider non sono limitati all'uso solo delle istanze Property, Feature, Option o ParameterInit definite nelle parole chiave dello schema di stampa nelle tecnologie compilate in Print Schema Framework. Le istanze di elemento specifiche del provider possono essere liberamente intercambiate all'interno di istanze di elemento definite nelle parole chiave dello schema di stampa. L'unico requisito è che le istanze di proprietà specifiche del provider (ovvero private) appartengano a uno spazio dei nomi chiaramente associato al provider.

-   [Stampare lo sfondo dello schema](print-schema-background.md)

-   [Tecnologie di Schema-Related stampa](print-schema-related-technologies.md)

-   [Termini usati nello schema di stampa](terms-used-in-the-print-schema.md)

-   [Sintassi dello schema di stampa](syntax-of-the-print-schema.md)

-   [Riepilogo dei tipi di elemento](summary-of-element-types.md)

-   [Framework dello schema di stampa](print-schema-framework.md)

-   [Parole chiave pubbliche dello schema di stampa](print-schema-public-keywords.md)

-   [Schema PrintCapabilities e costruzione di documenti](printcapabilities-schema-and-document-construction.md)

-   [Schema PrintTicket e costruzione di documenti](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



