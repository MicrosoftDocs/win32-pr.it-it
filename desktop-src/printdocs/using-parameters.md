---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Utilizzo di parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fe8fc7c79ed27c467b59ef67132e816cdcd63
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234567"
---
# <a name="using-parameters"></a>Utilizzo di parametri

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Oltre a assegnare un punteggio corretto a un'opzione che contiene istanze di ParameterRef (vedere [parametri di riferimento](referencing-parameters.md)), i provider PrintCapabilities o PrintTicket e i client devono essere preparati a gestire le situazioni seguenti che coinvolgono parametri.

I client dell'interfaccia utente devono richiedere all'utente di fornire inizializzatori di parametro (valori per gli elementi ParameterInit) per i parametri designati al momento appropriato, in modo che gli elementi ParameterInit appropriati vengano inseriti nel PrintTicket. I client dell'interfaccia utente devono essere in grado di distinguere i due tipi di parametri, in modo incondizionatamente obbligatorio e condizionale, e devono essere in grado di gestire ogni tipo in modo appropriato. Per un parametro obbligatorio in modo non condizionale, l'interfaccia utente deve assicurarsi che venga fornito un elemento ParameterInit per questo tipo di parametro. Per un parametro obbligatorio in modo condizionale, l'interfaccia utente deve fornire un valore ParameterInit se il parametro viene usato come riferimento da un'opzione selezionata nell'oggetto PrintTicket. Lo stato obbligatorio di un parametro è specificato in un'istanza di ParameterDef. Per altre informazioni, vedere [elementi ParameterDef e ParameterInit](parameterdef-and-parameterinit-elements.md). I client dell'interfaccia utente devono convalidare i valori ParameterInit specificati dall'utente per verificare che soddisfino i requisiti specificati nell'istanza di ParameterDef.

I provider PrintTicket devono inoltre controllare le istanze di ParameterInit fornite da PrintTicket per verificare che tutti i parametri necessari siano presenti e soddisfino i requisiti specificati nell'istanza di ParameterDef. Il codice di convalida deve fornire impostazioni predefinite ragionevoli nel caso in cui i valori di ParameterInit non siano validi o mancanti. Si noti che un ParameterDef consente di fornire un valore predefinito a questo scopo. Inoltre, se sono presenti vincoli che coinvolgono i parametri, ad esempio, "Se *CopyCount* è maggiore di N, non usare un contenitore di input con capacità ridotta", il codice di convalida PrintTicket deve rilevare questo vincolo e modificare il PrintTicket per evitare di attivare il vincolo.

Se è presente una dipendenza dell'oggetto PrintCapabilities sui parametri specificati nell'oggetto PrintTicket, i provider PrintCapabilities devono monitorare i valori ParameterInit e produrre un documento PrintCapabilities appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



