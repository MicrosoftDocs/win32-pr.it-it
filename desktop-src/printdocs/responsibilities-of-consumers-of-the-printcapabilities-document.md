---
description: I consumer di documenti PrintCapabilities hanno determinati obblighi che devono rispettare prima di poter usare un documento PrintCapabilities.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilità dei consumer del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49cd8f843bfa39a4313b0958fe9874f1263403e3fb3b2f22e2c965927bf6f25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470253"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Responsabilità dei consumer del documento PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I consumer di documenti PrintCapabilities hanno determinati obblighi che devono rispettare prima di poter usare un documento PrintCapabilities. I requisiti seguenti si applicano ai client di un documento PrintCapabilities.

-   Non devono rifiutare o non riuscire a elaborare printcapabilities sintatticamente validi; in altre informazioni, qualsiasi documento PrintCapabilities conforme allo schema PrintCapabilities.

-   Devono essere in grado di risolvere la presenza imprevista o l'assenza di contenuto definito privatamente. È incluso il contenuto definito privatamente che viene visualizzato all'interno di istanze di elementi definiti dello schema di stampa.

-   Devono essere in grado di aggirare il contenuto facoltativo dello schema di stampa assente.

-   Devono sapere quando richiedere un nuovo documento.

    -   I valori delle istanze property sono dipendenti dalla configurazione (di conseguenza, dipendenti da snapshot). È necessario aggiornare lo snapshot quando si accede a un'istanza property.

    -   Le istanze Feature, Option e ScoredProperty che devono essere copiate in printTicket sono statiche per definizione. Ovvero, non dipendono (e non devono) dipendere dalla configurazione del dispositivo. Se si accede a istanze di questi tipi, non è necessario ottenere un nuovo documento PrintCapabilities quando la configurazione viene modificata.

-   I consumer di PrintCapabilities che sono client dell'interfaccia utente devono essere in grado di usare le informazioni in un documento PrintCapabilities per costruire un'interfaccia utente e per costruire un PrintTicket valido dalle selezioni dell'utente. Ciò include la conoscenza delle istanze ParameterInit da specificare e la convalida delle istanze specificate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



