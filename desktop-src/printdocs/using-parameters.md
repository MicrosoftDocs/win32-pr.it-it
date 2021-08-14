---
description: Informazioni sull'uso dei parametri in un documento PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Utilizzo di parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc19b6c2b6deb269c0d3a34140bc0e9816febc86d33adfdb6ed0c91fe38f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469326"
---
# <a name="using-parameters"></a>Utilizzo di parametri

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Oltre a segnare correttamente un'opzione che contiene istanze ParameterRef (vedere Parametri di [riferimento),](referencing-parameters.md)i provider e i client PrintCapabilities o PrintTicket devono essere preparati a gestire le situazioni seguenti che coinvolgono i parametri.

I client dell'interfaccia utente devono richiedere all'utente di fornire inizializzatori di parametro (valori per gli elementi ParameterInit) per i parametri designati al momento appropriato in modo che gli elementi ParameterInit appropriati siano inseriti in PrintTicket. I client dell'interfaccia utente devono essere in grado di distinguere i due tipi di parametri, incondizionatamente obbligatorio e condizionale, e devono essere in grado di gestire ogni tipo in modo appropriato. Per un parametro obbligatorio incondizionatamente, l'interfaccia utente deve garantire che per questo tipo di parametro sia specificato un elemento ParameterInit. Per un parametro obbligatorio condizionale, l'interfaccia utente deve fornire un valore ParameterInit se al parametro viene fatto riferimento da un'opzione selezionata in PrintTicket. Lo stato Obbligatorio di un parametro viene specificato in un'istanza ParameterDef. Per altre informazioni, vedere [Elementi ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md). I client dell'interfaccia utente devono convalidare i valori ParameterInit forniti dall'utente per verificare che soddisfino i requisiti specificati nell'istanza di ParameterDef.

I provider PrintTicket devono anche controllare le istanze ParameterInit fornite da PrintTicket per verificare che siano presenti tutti i parametri necessari e che soddisfino i requisiti specificati nell'istanza ParameterDef. Il codice di convalida deve fornire valori predefiniti ragionevoli nel caso in cui i valori ParameterInit non siano validi o mancanti. Si noti che un oggetto ParameterDef consente di ottenere un valore predefinito a questo scopo. Inoltre, se sono presenti vincoli che coinvolgono i parametri, ad esempio "se *CopyCount* è maggiore di N, non usare un contenitore di input con capacità ridotta", il codice di convalida PrintTicket deve rilevare questo vincolo e modificare PrintTicket per evitare di attivare il vincolo.

Se esiste una dipendenza di PrintCapabilities dai parametri specificati in PrintTicket, i provider PrintCapabilities devono monitorare i valori ParameterInit e produrre un documento PrintCapabilities appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



