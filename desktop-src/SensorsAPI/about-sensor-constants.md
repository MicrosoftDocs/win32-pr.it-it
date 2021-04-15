---
description: Informazioni sulle costanti del sensore
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Informazioni sulle costanti del sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea862d38af74058d11d3a6fa1eb11a702b3b277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529874"
---
# <a name="about-sensor-constants"></a>Informazioni sulle costanti del sensore

La piattaforma sensore e posizione di Windows utilizza le costanti in molti modi. La piattaforma definisce costanti diverse che è possibile usare nel codice del driver del sensore. I produttori di sensori possono definire costanti personalizzate. È possibile trovare le definizioni delle costanti definite dalla piattaforma nel file Sensors. h. Per informazioni dettagliate sulle costanti dei sensori definite dalla piattaforma, vedere [costanti](constants.md).

### <a name="sensor-and-data-organization"></a>Sensore e organizzazione dei dati

La piattaforma organizza i sensori e i dati nei modi seguenti.

-   Le categorie rappresentano classi generali di dispositivi sensori. Le categorie consentono di raggruppare i sensori che probabilmente forniscono tipi simili di informazioni o in qualche modo correlati. Ogni categoria è rappresentata da una costante **GUID** . Ad esempio, i sensori che segnalano le coordinate di latitudine e Longitudine appartengono alla categoria del sensore di posizione. Questo è representented dalla costante di \_ posizione della categoria del sensore \_ .
-   I tipi di sensore rappresentano tipi specifici di sensori. Ogni tipo di sensore si inserisce in una categoria specifica. Due sensori di tipi diversi possono appartenere alla stessa categoria o a categorie diverse. Ogni tipo di sensore è rappresentato da una costante **GUID** . Un sensore di sistema di posizionamento globale, ad esempio, verrebbe identificato dalla \_ costante GPS del percorso del tipo di sensore \_ \_ . Tuttavia, un sensore che fornisce la posizione corrente usando un indirizzo IP verrebbe identificato dalla costante di ricerca del \_ percorso del tipo di sensore \_ \_ . Tuttavia, entrambi i sensori appartengono alla categoria del sensore della posizione.
-   I tipi di dati rappresentano tipi specifici di informazioni che possono essere fornite dal sensore. I tipi di dati dei sensori possono contenere il valore di misurazione effettivo, ad esempio Altitude; informazioni sulle unità usate per esprimere i dati, ad esempio i contatori; e punti di riferimento per i dati, ad esempio il livello Sea. Ogni tipo di dati è rappresentato da una costante **PropertyKey** . Ad esempio, il tipo di dati che rappresenta l'altitudine sopra il livello del mare, in metri, verrebbe identificato dal tipo di dati del sensore di \_ \_ \_ altitudine \_ altitudine \_ metri costante.
-   Quando si segnalano dati, un valore viene definito contenuto in un campo dati e una raccolta di campi dati correlati costituisce un report dati. I report di dati vengono assemblati insieme usando l'interfaccia [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) . Ogni report dati deve contenere almeno un campo dati valido e un timestamp che identifichi il momento in cui è stato creato il report dati. I timestamp sono rappresentati dalla \_ costante timestamp del tipo di dati del sensore \_ \_ .

### <a name="other-constants"></a>Altre costanti

Il programma deve usare anche altre costanti. Queste costanti includono quanto segue:

-   Proprietà del sensore, ad esempio \_ Descrizione della proprietà del sensore \_ . In genere, queste costanti vengono usate per descrivere un sensore. Alcune proprietà del sensore devono essere fornite dal sensore, alcune proprietà possono essere impostate dalle applicazioni client, mentre altre devono sempre restituire lo stesso valore dal sensore. La sezione di riferimento delle [**proprietà dei sensori**](sensor-properties.md) fornisce queste informazioni per ogni proprietà.
-   Costanti di evento, ad esempio \_ lo stato dell'evento del sensore \_ \_ modificato. Le costanti di evento includono **GUID**, che rappresentano i tipi di eventi e **PropertyKey** s, che rappresentano i tipi di parametro dell'evento. Queste costanti vengono usate per le chiamate al metodo, ad esempio [**ISensor:: SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) e [**ISensor:: GetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest).

### <a name="custom-constants"></a>Costanti personalizzate

I produttori di sensori possono definire costanti personalizzate. Un sensore, ad esempio, può appartenere a una categoria non definita dalla piattaforma. Prima di poter usare un sensore che definisce costanti personalizzate, il produttore del sensore deve pubblicare i valori, ad esempio pubblicando un file di intestazione. Per ulteriori informazioni, vedere la documentazione fornita con il sensore.

 

 
