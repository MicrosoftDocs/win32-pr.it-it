---
description: Questa panoramica della funzionalità PrintTicket descrive il formato per esprimere le informazioni di configurazione del dispositivo e l'uso di un PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Panoramica della funzionalità PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd01e7247de83e8f378dbcff8e99c32abacd448f436ad69af1f99a1566655b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718971"
---
# <a name="overview-of-printticket-functionality"></a>Panoramica della funzionalità PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

PrintTicket usa un formato basato su XML per esprimere le informazioni di configurazione del dispositivo usando i costrutti di funzionalità/opzione e parametri di Print Schema Framework. Sono inclusi tutti i tipi di elemento standard, nonché le funzionalità di estendibilità del framework dello schema di stampa. Si presuppone che printTicket sia una descrizione autonoma della modalità di elaborazione di una singola pagina. I passaggi necessari per estrarre e costruire un PrintTicket di questo tipo da un particolare formato di documento non sono trattati qui.

Un PrintTicket può essere usato per ottenere un documento PrintCapabilities che descrive le caratteristiche del dispositivo per una particolare configurazione. In alternativa, è possibile inviare PrintTicket con un set di istruzioni per il rendering per produrre una pagina di output sottoposta a rendering ed elaborata in base alla configurazione specificata in PrintTicket.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



