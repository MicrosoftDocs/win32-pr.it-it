---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Elenchi di controllo di costruzione PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320851"
---
# <a name="printticket-construction-checklists"></a>Elenchi di controllo di costruzione PrintTicket

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In questa sezione viene illustrato come l'autore di un client PrintTicket può utilizzare i tipi di elemento definiti nel Framework dello schema di stampa per creare un oggetto PrintTicket che descriva le finalità di un dispositivo. L'oggetto PrintTicket può essere generico (non associato a un dispositivo specifico) o può essere specifico del dispositivo. La semantica dell'oggetto PrintTicket viene presentata in modo più dettagliato. Questa sezione contiene inoltre una panoramica dei concetti e della terminologia trattati in modo più approfondito nelle sezioni successive.

Esistono due approcci fondamentalmente diversi alla costruzione di un oggetto PrintTicket. È possibile utilizzare entrambi gli approcci.

-   Destinare l'oggetto PrintTicket a un dispositivo sconosciuto o generico [creando un oggetto PrintTicket generico](creating-a-generic-printticket.md).

    Se l'obiettivo principale è quello di mantenere l'intento dell'utente finale, è consigliabile adottare questo approccio, costruendo e archiviando un oggetto PrintTicket generico non convalidato con il documento.

-   Destinare l'oggetto PrintTicket a un dispositivo specifico, [creando un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Se si è più interessati a sfruttare tutte le funzionalità offerte da un particolare dispositivo, è consigliabile adottare questo approccio, costruendo un oggetto PrintTicket per il dispositivo specifico e archiviando l'oggetto PrintTicket convalidato con il documento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



