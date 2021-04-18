---
description: Lo schema di stampa e le tecnologie correlate sono disponibili in Microsoft .NET Framework 3,0 e versioni successive di Microsoft .NET Framework e in Windows Vista e nelle versioni successive di Windows.
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: Stampa schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320850"
---
# <a name="print-schema"></a>Stampa schema

Lo schema di stampa e le tecnologie correlate sono disponibili in Microsoft .NET Framework 3,0 e versioni successive di Microsoft .NET Framework e in Windows Vista e nelle versioni successive di Windows. I documenti XPS e il modello a oggetti XPS possono utilizzare gli oggetti Print Ticket, descritti nella [specifica Print Schema](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip), per specificare le preferenze di stampa di un documento per le stampanti e la visualizzazione delle applicazioni.

La [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) è un documento scaricabile che contiene informazioni sullo schema di stampa e su come usarlo in documenti e stampa. Informazioni aggiuntive sono disponibili online solo per le informazioni, in [riferimento allo schema di stampa legacy](print-schema.md); Tuttavia, potrebbe non riflettere accuratamente la versione corrente della [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Per informazioni sulla progettazione più aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) .

## <a name="print-schema-overview"></a>Panoramica dello schema di stampa

Lo schema di stampa è un schema basato su XML e strutturato in modo gerarchico che consente di organizzare e descrivere le proprietà di una stampante o di un processo di stampa. Lo schema di stampa include due componenti: le parole chiave dello schema di stampa e il Framework dello schema di stampa. Le parole chiave dello schema di stampa sono un set di istanze di elementi che descrivono gli attributi della stampante e lo scopo di formattazione dei processi di stampa Il Framework dello schema di stampa definisce una raccolta strutturata gerarchica di tipi di elemento XML e il modo in cui questi tipi di elemento possono essere utilizzati insieme.

Le tecnologie dello schema di stampa, denominate *PrintCapabilities* e *PrintTicket*, vengono compilate utilizzando le parole chiave Print Schema come specificato dal Framework Print Schema. La specifica dello schema di stampa supporta le estensioni dello schema di terze parti, in modo che gli utenti dello schema di stampa non siano limitati alle istanze di proprietà, funzionalità, opzione o ParameterInit definite dalle parole chiave dello schema di stampa. È possibile aggiungere istanze di elementi di terze parti alle istanze degli elementi definite dalle parole chiave Print Schema. le istanze di proprietà private di terze parti, tuttavia, devono appartenere a uno spazio dei nomi che è chiaramente associato alla terza parte che ha creato lo spazio dei nomi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Riferimento allo schema di stampa legacy](print-schema.md)
</dt> <dt>

[Comunicazione bidirezionale stampanti (hardware Dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
