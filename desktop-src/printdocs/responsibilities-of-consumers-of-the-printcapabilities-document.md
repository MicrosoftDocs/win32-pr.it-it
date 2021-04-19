---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilità degli utenti del documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320953"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Responsabilità degli utenti del documento PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Gli utenti dei documenti PrintCapabilities hanno determinati obblighi che devono sostenere per poter usare un documento PrintCapabilities. I requisiti seguenti si applicano ai client di un documento PrintCapabilities.

-   Non devono rifiutare o non riuscire a elaborare elementi PrintCapabilities sintatticamente validi; ovvero qualsiasi documento PrintCapabilities conforme allo schema PrintCapabilities.

-   Devono essere in grado di aggirare la presenza imprevista o l'assenza di contenuto definito privatamente. Questo include contenuto definito privatamente che viene visualizzato all'interno di istanze di elementi di stampa definiti dallo schema.

-   Devono essere in grado di aggirare il contenuto facoltativo dello schema di stampa che è assente.

-   Devono essere consapevoli del momento in cui richiedere un nuovo documento.

    -   I valori delle istanze di proprietà sono dipendenti dalla configurazione, quindi dipendenti dallo snapshot. Quando si accede a un'istanza di proprietà, è necessario aggiornare lo snapshot.

    -   Le istanze di feature, Option e ScoredProperty che devono essere copiate in un oggetto PrintTicket sono statiche per definizione. Ovvero non sono (e non devono essere) dipendenti dalla configurazione del dispositivo. Se si accede a tutte le istanze di questi tipi, non è necessario ottenere un nuovo documento PrintCapabilities quando viene modificata la configurazione.

-   I consumer di PrintCapabilities che sono client dell'interfaccia utente devono essere in grado di utilizzare le informazioni in un documento PrintCapabilities per costruire un'interfaccia utente e costruire un oggetto PrintTicket valido dalle selezioni dell'utente. Ciò include la conoscenza delle istanze di ParameterInit che è necessario specificare e la convalida delle istanze specificate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



