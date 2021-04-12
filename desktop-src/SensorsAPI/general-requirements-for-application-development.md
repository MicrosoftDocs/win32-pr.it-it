---
description: Questo argomento descrive cosa è necessario fare per iniziare a creare programmi che usano l'API del sensore.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisiti generali per lo sviluppo di applicazioni (API dei sensori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347646"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Requisiti generali per lo sviluppo di applicazioni (API dei sensori)

Questo argomento descrive cosa è necessario fare per iniziare a creare programmi che usano l'API del sensore.

Per creare un'applicazione API per i sensori, è necessario installare Windows 7 e il Software Development Kit (SDK) di Windows 7 nel computer. Nella tabella seguente vengono descritti i file specifici necessari.



| Nome file               | Descrizione                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi. h            | Il file di intestazione principale per l'API del sensore. Questo file di intestazione contiene le definizioni dell'interfaccia.               |
| Sensori. h               | Il file di intestazione che contiene le definizioni delle costanti definite dalla piattaforma.                                    |
| Initguid. h              | Il file di intestazione che contiene le definizioni per il controllo dell'inizializzazione del **GUID** .                          |
| FunctionDiscoveryKeys. h | Il file di intestazione che definisce le chiavi della proprietà ID dispositivo necessarie quando ci si connette ai sensori logici. |
| Sensorsapi. lib          | Libreria statica che contiene le definizioni **GUID** per l'API del sensore.                                     |
| PortableDeviceGuids. lib | Libreria statica che contiene le definizioni **GUID** per gli oggetti dispositivi portatili Windows.                   |



 

Il programma potrebbe richiedere file aggiuntivi.

## <a name="supported-operating-systems"></a>Sistemi operativi supportati

Le applicazioni dell'API del sensore vengono eseguite in tutte le edizioni di Windows 7, ad eccezione di Windows 7 Starter Edition.

## <a name="windows-portable-devices-interfaces"></a>Interfacce dei dispositivi portatili Windows

L'API dei sensori USA determinati oggetti dispositivi portatili Windows (WPD) per incapsulare le chiavi e i valori delle proprietà. Nella tabella seguente vengono descritte le interfacce per questi oggetti.



| Interfaccia                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Questa interfaccia fornisce un modo pratico per creare un contenitore di proprietà di coppie nome/valore. I nomi sono rappresentati da **PropertyKey** e i valori sono rappresentati da **PROPVARIANT** s. <br/> L'API usa questa interfaccia per l'impostazione e il recupero di valori singoli e set di valori. Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamando **CoCreateInstance** con CLSID \_ PortableDeviceValues.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Questa interfaccia contiene una raccolta di **PropertyKey** s. Queste chiavi rappresentano i nomi di proprietà che possono essere archiviati da **IPortableDeviceValues**. L'API usa questo oggetto raccolta per impostare e recuperare sia i nomi di proprietà singoli che i set di nomi di proprietà.<br/> Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamando **CoCreateInstance** con CLSID \_ PortableDeviceKeyCollection. <br/>    |



 

 

