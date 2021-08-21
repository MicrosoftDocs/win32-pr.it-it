---
description: I sensori logici forniscono dati senza dipendere dai dispositivi hardware.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Informazioni sui sensori logici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bb7a6e67223bb959b155e55f6cc059ffd8280bc8c08fb00d4d88cb2c8b0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003894"
---
# <a name="about-logical-sensors"></a>Informazioni sui sensori logici

*I sensori logici* forniscono dati senza dipendere dai dispositivi hardware. Ad esempio, un sensore logico può fornire dati sulla posizione corrente dell'utente usando un servizio che cerca un indirizzo IP in una tabella. I sensori logici vengono implementati come driver dei sensori. Per informazioni su come implementare un driver di sensore, vedere il kit Windows Driver Kit.

Dopo aver installato un sensore logico nel computer dell'utente, è possibile usarlo allo stesso modo di un sensore basato su hardware. L'API Sensor fornirà [**un'interfaccia ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) per rappresentare il sensore logico e il programma può richiedere dati tramite gli stessi meccanismi che si userebbero per qualsiasi altro tipo di sensore. I sensori logici possono anche usare le categorie, i tipi, i tipi di dati, le proprietà e gli eventi dei sensori definiti dalla piattaforma. Oppure è possibile definire valori personalizzati.

[**L'interfaccia ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) consente agli sviluppatori che creano sensori logici di gestire le connessioni alla piattaforma Sensor e Location.

> [!Note]  
> Come per altri driver, l'installazione o la disinstallazione di un driver del sensore logico richiede privilegi di amministratore.

 

Per provare a usare un sensore logico di esempio, vedere [Informazioni sugli esempi e sugli strumenti](about-the-samples.md).

## <a name="managing-logical-sensors"></a>Gestione dei sensori logici

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) ha i metodi seguenti:

-   [**Connettere**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Disconnetti**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Disinstallare**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Quando si chiama [**Connessione**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)), l'API Sensor crea un'istanza del driver del sensore, se non esiste già, e quindi connette il sensore logico alla piattaforma. Ciò significa che il sensore logico viene visualizzato con altri sensori nel Sensore di posizione e altri sensori **Pannello di controllo.** Quando si chiama [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), l'API Sensor disconnette il sensore logico e lo rimuove dal Pannello di controllo. La **chiamata di** Disconnect non rimuove il sensore logico da Gestione **dispositivi.** Pertanto, le chiamate future **a Connessione** si trasporteranno in una connessione molto più veloce al sensore logico.

Per rimuovere un sensore logico, è necessario chiamare [**Disinstalla**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). La disinstallazione di un sensore logico rimuove il sensore **da Gestione dispositivi**. Poiché i dispositivi del sensore logico esistono solo in memoria, un sensore logico viene disinstallato quando l'utente Windows.

L'API Sensor identifica un determinato sensore logico in base al *relativo ID logico,* ovvero un **GUID**. Ogni volta che ci si connette a un sensore logico specifico, è necessario fornire un ID logico. Ogni volta che si disconnette o disinstalla un sensore specifico, è necessario specificare lo stesso ID logico usato per la connessione. Se ci si connette più volte allo stesso driver del sensore logico usando ID logici diversi, si creerà un'istanza separata del sensore logico per ogni nuovo ID logico. Anche se si chiama [**Disconnetti**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) per ogni ID logico, [](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) queste istanze separate rimarranno in **Gestione** dispositivi fino a quando non si chiama Disinstalla per ogni sensore logico o l'utente non Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di sensori logici](using-logical-sensors.md)
</dt> </dl>

 

 
