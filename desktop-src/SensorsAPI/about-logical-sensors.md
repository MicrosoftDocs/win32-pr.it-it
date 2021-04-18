---
description: I sensori logici forniscono dati senza dipendere da dispositivi hardware.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Informazioni sui sensori logici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6f8687575aaedbb006eb2ad6ebaad9cf8d3ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316622"
---
# <a name="about-logical-sensors"></a>Informazioni sui sensori logici

I *sensori logici* forniscono dati senza dipendere da dispositivi hardware. Un sensore logico, ad esempio, può fornire dati sulla posizione corrente dell'utente usando un servizio che cerca un indirizzo IP in una tabella. I sensori logici vengono implementati come driver del sensore. Per informazioni sull'implementazione di un driver del sensore, vedere Windows Driver Kit.

Quando un sensore logico viene installato nel computer dell'utente, è possibile usarlo nello stesso modo in cui si trova un sensore basato su hardware. L'API del sensore fornirà un'interfaccia [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) per rappresentare il sensore logico e il programma potrà richiedere i dati attraverso gli stessi meccanismi usati per qualsiasi altro tipo di sensore. I sensori logici possono usare anche le categorie, i tipi, i tipi di dati, le proprietà e gli eventi del sensore definito dalla piattaforma. In alternativa, è possibile definire valori personalizzati.

L'interfaccia [**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) consente agli sviluppatori che creano sensori logici di gestire le connessioni alla piattaforma sensore e posizione.

> [!Note]  
> Come per gli altri driver, l'installazione o la disinstallazione di un driver del sensore logico richiede privilegi di amministratore.

 

Per provare a usare un sensore logico di esempio, vedere [informazioni sugli esempi e sugli strumenti](about-the-samples.md).

## <a name="managing-logical-sensors"></a>Gestione dei sensori logici

Per [**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) sono disponibili i metodi seguenti:

-   [**Connettersi**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Disconnetti**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Disinstallare**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Quando si chiama [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)), l'API Sensor crea un'istanza del driver del sensore, se non ne esiste già una, quindi connette il sensore logico alla piattaforma. Ciò significa che il sensore logico viene visualizzato con altri sensori nella **posizione e in altri sensori** del pannello di controllo. Quando si chiama [**Disconnetti**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), l'API del sensore disconnette il sensore logico e lo rimuove dal pannello di controllo. La chiamata di **Disconnect** non rimuove il sensore logico dal **Gestione dispositivi**. Pertanto, le chiamate future alla **connessione** comporteranno una connessione molto più rapida al sensore logico.

Per rimuovere un sensore logico, è necessario chiamare [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). La disinstallazione di un sensore logico rimuove il sensore dal **Gestione dispositivi**. Poiché i dispositivi dei sensori logici esistono solo in memoria, un sensore logico viene disinstallato quando l'utente riavvia Windows.

L'API del sensore identifica un determinato sensore logico in base al relativo *ID logico*, ovvero un **GUID**. Ogni volta che ci si connette a un determinato sensore logico, è necessario fornire un ID logico. Ogni volta che si disconnette o si disinstalla un particolare sensore, è necessario fornire lo stesso ID logico usato per la connessione. Se ci si connette più volte allo stesso driver del sensore logico utilizzando ID logici diversi, sarà necessario creare un'istanza separata del sensore logico per ogni nuovo ID logico. Anche se si chiama [**Disconnetti**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) per ogni ID logico, queste istanze separate rimarranno in **Gestione dispositivi** fino a quando non si chiama [**Disinstalla**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) per ogni sensore logico o l'utente riavvia Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di sensori logici](using-logical-sensors.md)
</dt> </dl>

 

 
