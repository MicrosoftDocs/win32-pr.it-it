---
description: Scopri in che modo l'autore di un client PrintTicket può usare i tipi di elemento per creare un PrintTicket che descrive le finalità di un dispositivo.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Elenchi di controllo per la costruzione di PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6a3ae0c19fea01738dbf7c6ecfa52f6f156d59f67dae89d6d5a2952059a765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091721"
---
# <a name="printticket-construction-checklists"></a>Elenchi di controllo per la costruzione di PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Questa sezione illustra come l'autore di un client PrintTicket può usare i tipi di elemento definiti in Print Schema Framework per creare un printTicket che descrive le finalità di un dispositivo. PrintTicket può essere generico (non associato a un dispositivo specifico) o specifico del dispositivo. La semantica di PrintTicket viene presentata in modo più dettagliato. Questa sezione contiene anche una panoramica dei concetti e della terminologia che vengono trattati in modo più approfondito nelle sezioni successive.

Esistono due approcci fondamentalmente diversi per la costruzione di un PrintTicket. È possibile usare entrambi gli approcci.

-   Impostare PrintTicket come destinazione di un dispositivo sconosciuto o generico [creando un printTicket generico.](creating-a-generic-printticket.md)

    Se l'obiettivo principale è mantenere la finalità dell'utente finale, è consigliabile adottare questo approccio, creando e archiviando un PrintTicket generico non convalidato con il documento.

-   Impostare PrintTicket come destinazione per un dispositivo specifico, creando [un Device-Specific PrintTicket.](creating-a-device-specific-printticket.md)

    Se si è più interessati a sfruttare tutte le funzionalità offerte da un particolare dispositivo, è possibile adottare questo approccio, creando un PrintTicket per il dispositivo specifico e archiviando il PrintTicket convalidato con il documento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



