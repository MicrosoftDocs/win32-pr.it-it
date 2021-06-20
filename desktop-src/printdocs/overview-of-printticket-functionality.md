---
description: Questa panoramica della funzionalità PrintTicket descrive il formato per esprimere le informazioni di configurazione del dispositivo e l'uso di un PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Panoramica della funzionalità PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408544"
---
# <a name="overview-of-printticket-functionality"></a>Panoramica della funzionalità PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

PrintTicket usa un formato basato su XML per esprimere le informazioni di configurazione del dispositivo usando i costrutti di funzionalità/opzione e di parametro di Print Schema Framework. Sono inclusi tutti i tipi di elemento standard, nonché le funzionalità di estendibilità del framework dello schema di stampa. Si presuppone che un PrintTicket sia una descrizione autonoma della modalità di elaborazione di una singola pagina. I passaggi necessari per estrarre e costruire un PrintTicket di questo tipo da un particolare formato di documento non sono trattati qui.

Un PrintTicket può essere usato per ottenere un documento PrintCapabilities che descrive le caratteristiche del dispositivo per una particolare configurazione. In alternativa, è possibile inviare PrintTicket con un set di istruzioni per il rendering per produrre una pagina di output sottoposta a rendering ed elaborata in base alla configurazione specificata in PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



