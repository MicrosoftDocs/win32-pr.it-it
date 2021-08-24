---
description: Messaggi di qualità
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Messaggi di qualità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15224e147d363a6cf3f3a55971d35a3d6596d95f07b9897ab1f258cc7febad48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747701"
---
# <a name="quality-messages"></a>Messaggi di qualità

I messaggi di qualità vengono definiti con la [**struttura Quality.**](/windows/win32/api/strmif/ns-strmif-quality) Questa struttura contiene i membri seguenti:

-   **Digitare:** Definito [**dall'enumerazione QualityMessageType.**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) Famine, che indica che il filtro sta ricevendo una quantità troppo piccola di dati, o Flood, che indica che il filtro sta ricevendo troppi dati.
-   **Proporzione:** Rettifica richiesta nella velocità dei dati, da una baseline di 1000. Ad esempio, 750 indica il 75% e 1500 indica il 150%.
-   **Ritardo:** Ora di riferimento che indica la data e l'ora di arrivo del campione più recente. Il valore è negativo se il campione è arrivato in anticipo.
-   **TimeStamp:** Timestamp dell'esempio più recente.

Si supponga, ad esempio, che un campione con un timestamp di 240 millisecondi (ms) raggiunga il renderer a 280 ms, tempo di flusso. Il renderer crea un messaggio di qualità di tipo Famine. L'esempio è arrivato 40 ms in ritardo, quindi il **membro Late** è 400000. Tutti i tempi di riferimento sono in unità di 100 nanosecondi. Il **membro TimeStamp** è 2400000.

Per il **membro Proportion,** il renderer potrebbe usare una media corrente per calcolare il valore. Forse i campioni sono arrivati in tempo e questo esempio è un'anomalia. In tal caso il renderer potrebbe richiedere solo una piccola correzione. D'altra parte, se i campioni sono costantemente in ritardo, il renderer potrebbe richiedere una correzione più grande.

Il controllo di qualità viene gestito tramite [**l'interfaccia IQualityControl.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) Contiene due metodi.

-   [**Notify:**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)invia un messaggio di qualità.
-   [**SetSink:**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)specifica un gestore qualità personalizzato.

Un oggetto che implementa **IQualityControl** riceve messaggi di qualità tramite il **relativo metodo Notify.** Può gestire il messaggio o passarlo a un altro oggetto. Se l'applicazione chiama il metodo **SetSink** dell'oggetto, l'oggetto deve delegare il controllo di qualità al gestore qualità specificato.

 

 



