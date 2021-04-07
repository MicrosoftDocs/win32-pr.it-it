---
description: La tabella CounterData contiene una riga per ogni contatore raccolto in un determinato momento. Il numero di queste righe sarà elevato.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: CounterData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881770"
---
# <a name="counterdata"></a>CounterData

La tabella **counterData** contiene una riga per ogni contatore raccolto in un determinato momento. Il numero di queste righe sarà elevato.

La tabella **counterData** definisce i campi seguenti:

-   **GUID:** GUID per questo set di dati. Usare questa chiave per unire in join la tabella [**DisplayToID**](displaytoid.md) .
-   **CounterID:** Identifica il contatore. Usare questa chiave per unire in join la tabella [**CounterDetails**](counterdetails.md) .
-   **RecordIndex:** Indice di esempio per un identificatore del contatore e un GUID della raccolta specifici. Il valore aumenta per ogni esempio successivo in questo file di log.
-   **CounterDateTime:** Ora in cui è stata avviata la raccolta, in ora UTC.
-   **CounterValue:** Valore formattato del contatore. Questo valore può essere zero per il primo record se il contatore richiede due esempi per calcolare un valore visualizzabile.
-   **FirstValueA:** Combinare questo valore a 32 bit con il valore di **FirstValueB** per creare il membro **FirstValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueA** contiene i bit di ordine inferiore.
-   **FirstValueB:** Combinare questo valore a 32 bit con il valore di **FirstValueA** per creare il membro **FirstValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueB** contiene i bit di ordine superiore.
-   **SecondValueA:** Combinare questo valore a 32 bit con il valore di **SecondValueB** per creare il membro **SecondValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueA** contiene i bit di ordine inferiore.
-   **SecondValueB:** Combinare questo valore a 32 bit con il valore di **SecondValueA** per creare il membro **SecondValue** del [**\_ \_ contatore PDH RAW**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueB** contiene i bit di ordine superiore.

I campi **GUID**, **CounterID** e **RecordIndex** costituiscono la chiave primaria per questa tabella.

 

 



