---
description: Messaggi di qualità
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Messaggi di qualità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521329"
---
# <a name="quality-messages"></a>Messaggi di qualità

I messaggi qualitativi vengono definiti con la struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) . Questa struttura contiene i membri seguenti:

-   **Tipo:** Definito dall'enumerazione [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) . entrambe le carestie, a indicare che il filtro sta ricevendo dati troppo piccoli o flood, a indicare che il filtro sta ricevendo troppi dati.
-   **Proporzione:** Regolazione richiesta nella velocità dati, da una linea di base 1000. 750 indica, ad esempio, 75% e 1500 indica il 150%.
-   In **ritardo:** Tempo di riferimento che indica la fine dell'arrivo dell'esempio più recente. Il valore è negativo se l'esempio è arrivato in anticipo.
-   **Timestamp:** Timestamp dell'esempio più recente.

Si supponga, ad esempio, che un campione con un timestamp di 240 millisecondi (MS) raggiunga il renderer a 280 MS, il flusso di tempo. Il renderer crea un messaggio qualitativo di tipo carestie. L'esempio è arrivato 40 ms tardi, quindi il membro **tardivo** è 400000. (Tutti i tempi di riferimento sono in unità di 100 nanosecondi). Il membro **timestamp** è 2,4 milioni.

Per il membro **proporzionale** , il renderer può utilizzare una media in esecuzione per calcolare il valore. Forse gli esempi sono arrivati in tempo e questo esempio è un'anomalia. In tal caso, il renderer potrebbe richiedere solo una piccola correzione. D'altra parte, se gli esempi sono costantemente tardi, il renderer potrebbe richiedere una correzione più grande.

Il controllo qualità viene gestito tramite l'interfaccia [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) . Contiene due metodi.

-   [**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Invia un messaggio di qualità.
-   [**SESINK**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): specifica un gestore qualità personalizzato.

Un oggetto che implementa **IQualityControl** riceve messaggi di qualità tramite il metodo **Notify** . Il messaggio può essere gestito o passato a un altro oggetto. Se l'applicazione chiama **il metodo SetValue dell'oggetto** , l'oggetto deve delegare il controllo qualità al gestore qualità specificato.

 

 



