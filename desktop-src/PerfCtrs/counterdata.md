---
description: La tabella CounterData contiene una riga per ogni contatore raccolto in un determinato momento. Sarà presente un numero elevato di queste righe.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Counterdata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b352b9ec6bde6e644d80e7556ac46211212b66b4d92601deedaecaa5dd07344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033991"
---
# <a name="counterdata"></a>Counterdata

La **tabella CounterData** contiene una riga per ogni contatore raccolto in un determinato momento. Sarà presente un numero elevato di queste righe.

La **tabella CounterData** definisce i campi seguenti:

-   **GUID:** GUID per questo set di dati. Usare questa chiave per creare un join con [**la tabella DisplayToID.**](displaytoid.md)
-   **CounterID:** Identifica il contatore. Usare questa chiave per creare un join con [**la tabella CounterDetails.**](counterdetails.md)
-   **RecordIndex:** Indice di esempio per un identificatore di contatore e un GUID di raccolta specifici. Il valore aumenta per ogni esempio successivo in questo file di log.
-   **CounterDateTime:** Ora di avvio della raccolta, in formato UTC.
-   **CounterValue:** Valore formattato del contatore. Questo valore può essere zero per il primo record se il contatore richiede due campioni per calcolare un valore visualizzabile.
-   **FirstValueA:** Combinare questo valore a 32 bit con il valore di **FirstValueB** per creare il **membro FirstValue** di [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueA** contiene i bit di ordine più basso.
-   **FirstValueB:** Combinare questo valore a 32 bit con il valore **di FirstValueA** per creare il **membro FirstValue** di [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueB** contiene i bit di ordine elevato.
-   **SecondValueA:** Combinare questo valore a 32 bit con il valore di **SecondValueB** per creare il membro **SecondValue** di [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueA** contiene i bit di ordine più basso.
-   **SecondValueB:** Combinare questo valore a 32 bit con il valore di **SecondValueA** per creare il **membro SecondValue** di [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueB** contiene i bit di ordine elevato.

I **campi GUID,** **CounterID** e **RecordIndex** costituiscono la chiave primaria per questa tabella.

 

 



