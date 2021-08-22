---
description: Informazioni sulle costanti del sensore
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Informazioni sulle costanti del sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cab8b5def4cdfa185a55dd993896fb5157563424b7753497413e5d7706465e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890256"
---
# <a name="about-sensor-constants"></a>Informazioni sulle costanti del sensore

La Windows Sensor and Location usa le costanti in molti modi. La piattaforma definisce costanti diverse che è possibile usare nel codice del driver del sensore. I produttori di sensori possono definire costanti personalizzate. Le definizioni delle costanti definite dalla piattaforma sono disponibili nel file Sensors.h. Per informazioni dettagliate sulle costanti dei sensori definite dalla piattaforma, vedere [Costanti.](constants.md)

### <a name="sensor-and-data-organization"></a>Organizzazione di sensori e dati

La piattaforma organizza i sensori e i dati nei modi seguenti.

-   Le categorie rappresentano ampie classi di dispositivi di sensori. Le categorie consentono di raggruppare sensori che probabilmente forniscono tipi simili di informazioni o che sono altrimenti correlati in qualche modo. Ogni categoria è rappresentata da una **costante GUID.** Ad esempio, i sensori che segnalano le coordinate di latitudine e longitudine appartengono alla categoria del sensore di posizione. Questo valore è rappresentato dalla costante SENSOR \_ CATEGORY \_ LOCATION.
-   I tipi di sensori rappresentano tipi specifici di sensori. Ogni tipo di sensore rientra in una categoria specifica. Due sensori di tipi diversi possono appartenere alla stessa categoria o a categorie diverse. Ogni tipo di sensore è rappresentato da una **costante GUID.** Ad esempio, un sensore del sistema di posizionamento globale verrebbe identificato dalla costante GPS SENSOR \_ TYPE \_ \_ LOCATION. Tuttavia, un sensore che fornisce la posizione corrente usando un indirizzo IP viene identificato dalla costante SENSOR \_ TYPE \_ LOCATION \_ LOOKUP. Tuttavia, entrambi i sensori appartengono alla categoria di sensori di posizione.
-   I tipi di dati rappresentano tipi specifici di informazioni che il sensore può fornire. I tipi di dati dei sensori possono contenere il valore effettivo della misura, ad esempio l'altitudine. informazioni sulle unità usate per esprimere i dati, ad esempio i contatori; e punti di riferimento per i dati, ad esempio il livello del mare. Ogni tipo di dati è rappresentato da una **costante PROPERTYKEY.** Ad esempio, il tipo di dati che rappresenta l'altitudine sopra il livello del mare, in metri, verrebbe identificato dalla costante SENSOR \_ DATA \_ TYPE ALTITUDE \_ \_ SEALEVEL \_ METERS.
-   Quando si segnalano dati, un valore viene detto contenuto in un campo dati e una raccolta di campi dati correlati costituiscono un report di dati. I report di dati vengono uniti tramite [l'interfaccia IPortableDeviceValues.](/previous-versions//ms740012(v=vs.85)) Ogni report di dati deve contenere almeno un campo dati valido e un timestamp che identifica quando è stato creato il report di dati. I timestamp sono rappresentati dalla costante SENSOR \_ DATA \_ TYPE \_ TIMESTAMP.

### <a name="other-constants"></a>Altre costanti

Il programma deve usare anche altre costanti. Queste costanti includono quanto segue:

-   Proprietà del sensore, ad esempio SENSOR \_ PROPERTY \_ DESCRIPTION. In genere, queste costanti vengono usate per descrivere un sensore. Alcune proprietà del sensore devono essere fornite dal sensore, alcune proprietà possono essere impostate dalle applicazioni client e altre devono sempre restituire lo stesso valore dal sensore. La [**sezione informazioni di**](sensor-properties.md) riferimento sulle proprietà del sensore fornisce queste informazioni per ogni proprietà.
-   Costanti di evento, ad esempio SENSOR \_ EVENT \_ STATE \_ CHANGED. Le costanti di evento **includono GUID,** che rappresentano tipi di eventi, e **PROPERTYKEY,** che rappresentano i tipi di parametro dell'evento. Queste costanti verranno usate per le chiamate ai metodi, ad esempio [**ISensor::SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) e [**ISensor::GetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest).

### <a name="custom-constants"></a>Costanti personalizzate

I produttori di sensori possono definire costanti personalizzate. Ad esempio, un sensore può appartenere a una categoria non definita dalla piattaforma. Prima di poter usare un sensore che definisce costanti personalizzate, il produttore del sensore deve pubblicare i valori, ad esempio pubblicando un file di intestazione. Per altre informazioni, vedere la documentazione fornita con il sensore.

 

 
