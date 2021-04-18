---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Riferimento allo schema di stampa legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320956"
---
# <a name="legacy-print-schema-reference"></a>Riferimento allo schema di stampa legacy

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa e le tecnologie correlate sono disponibili in Microsoft .NET Framework 3,0, Microsoft Windows Vista e versioni successive.

Lo schema di stampa fornisce un formato basato su XML per esprimere e organizzare un ampio set di proprietà che descrivono un formato di processo o PrintCapabilities in modo gerarchico.

Lo schema di stampa è un termine che include due componenti, ovvero le parole chiave dello schema di stampa e il Framework dello schema di stampa. Il documento parole chiave di Print Schema è uno schema pubblico che definisce un set di istanze di elementi che possono essere usate per descrivere gli attributi del dispositivo e la formattazione del processo di stampa. Print Schema Framework è uno schema pubblico che definisce una raccolta strutturata gerarchica di tipi di elemento XML e specifica come i tipi di elemento possono essere utilizzati insieme.

Le parole chiave dello schema di stampa e il Framework dello schema di stampa costituiscono la base per due tecnologie correlate allo schema di stampa, lo schema PrintCapabilities e lo schema PrintTicket.

È importante tenere presente che uno degli obiettivi dello schema di stampa è quello di supportare le estensioni dello schema per provider. Ovvero i provider non sono limitati all'utilizzo solo delle istanze di proprietà, funzionalità, opzione o ParameterInit definite nelle parole chiave dello schema di stampa nelle tecnologie compilate nel Framework dello schema di stampa. Le istanze degli elementi specifiche del provider possono essere liberamente sparpagliate nelle istanze degli elementi definite nelle parole chiave Print Schema. L'unico requisito è che le istanze di proprietà specifiche del provider (ovvero private) devono appartenere a uno spazio dei nomi che è chiaramente associato al provider.

-   [Sfondo dello schema di stampa](print-schema-background.md)

-   [Tecnologie Schema-Related di stampa](print-schema-related-technologies.md)

-   [Termini usati nello schema di stampa](terms-used-in-the-print-schema.md)

-   [Sintassi dello schema di stampa](syntax-of-the-print-schema.md)

-   [Riepilogo dei tipi di elemento](summary-of-element-types.md)

-   [Print Schema Framework](print-schema-framework.md)

-   [Parole chiave pubbliche dello schema di stampa](print-schema-public-keywords.md)

-   [Struttura del documento e dello schema PrintCapabilities](printcapabilities-schema-and-document-construction.md)

-   [Schema e costruzione di documenti PrintTicket](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



