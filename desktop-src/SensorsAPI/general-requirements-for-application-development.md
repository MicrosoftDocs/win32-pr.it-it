---
description: Questo argomento descrive cosa è necessario fare per iniziare a creare programmi che usano l'API Sensor.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisiti generali per lo sviluppo di applicazioni (API Sensor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148057cd837e8eef26e73ff9cdef07ca01c70cb4a107e5f6e77f9ca43487407d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003779"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Requisiti generali per lo sviluppo di applicazioni (API Sensor)

Questo argomento descrive cosa è necessario fare per iniziare a creare programmi che usano l'API Sensor.

Per creare un'applicazione dell'API Sensor, è necessario installare Windows 7 e Windows 7 Software Development Kit (SDK) nel computer. Nella tabella seguente vengono descritti i file specifici necessari.



| Nome file               | Descrizione                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi.h            | File di intestazione principale per l'API Sensor. Questo file di intestazione contiene le definizioni di interfaccia.               |
| Sensors.h               | File di intestazione che contiene le definizioni delle costanti definite dalla piattaforma.                                    |
| Initguid.h              | File di intestazione che contiene le definizioni per il controllo **dell'inizializzazione GUID.**                          |
| FunctionDiscoveryKeys.h | File di intestazione che definisce le chiavi di proprietà dell'ID dispositivo necessarie per la connessione ai sensori logici. |
| Sensorsapi.lib          | Libreria statica che contiene le **definizioni GUID** per l'API Sensor.                                     |
| PortableDeviceGuids.lib | Libreria statica che contiene **definizioni GUID** per Windows dispositivi portatili.                   |



 

Il programma potrebbe richiedere file aggiuntivi.

## <a name="supported-operating-systems"></a>Sistemi operativi supportati

Le applicazioni dell'API Sensor verranno eseguite in tutte le edizioni di Windows 7, ad Windows 7 Starter edizione.

## <a name="windows-portable-devices-interfaces"></a>Windows Interfacce per dispositivi portatili

L'API Sensor usa alcuni Windows WPD (Portable Devices) per incapsulare chiavi e valori di proprietà. Nella tabella seguente vengono descritte le interfacce per questi oggetti.



| Interfaccia                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Questa interfaccia offre un modo pratico per creare un contenitore di proprietà di coppie nome/valore. I nomi sono rappresentati **da PROPERTYKEY** s e i valori sono rappresentati da **PROPVARIANT** s. <br/> L'API usa questa interfaccia per impostare e recuperare sia valori singoli che set di valori. Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamando **CoCreateInstance** con CLSID \_ PortableDeviceValues.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Questa interfaccia contiene una raccolta di **PROPERTYKEY** s. Queste chiavi rappresentano i nomi delle proprietà che possono essere archiviati **da IPortableDeviceValues.** L'API usa questo oggetto raccolta per l'impostazione e il recupero di nomi di singole proprietà e set di nomi di proprietà.<br/> Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamando **CoCreateInstance** con CLSID \_ PortableDeviceKeyCollection. <br/>    |



 

 

