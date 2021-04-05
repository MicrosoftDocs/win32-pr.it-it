---
description: Interfacce client
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Interfacce client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7c85ec5cb9b35e30d68b1d784cdebf230fdaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883169"
---
# <a name="client-interfaces"></a>Interfacce client

Le applicazioni utilizzano i metodi supportati dalle interfacce seguenti per eseguire operazioni sui dispositivi portatili. Queste operazioni includono l'apertura di una connessione a un dispositivo, il recupero di dati da un dispositivo, la scrittura di dati in un dispositivo e così via.



| Interfaccia                                                                              | Descrizione                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Enumera gli oggetti in un dispositivo portatile.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Fornisce accesso di basso livello a un dispositivo portatile.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Recupera un'ampia gamma di funzionalità del dispositivo, inclusi i formati supportati, i comandi e gli oggetti funzionali.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Fornisce metodi per creare, enumerare ed eliminare contenuto in un dispositivo.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Espone metodi aggiuntivi su un **IStream** usato per i trasferimenti di dati.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Implementata dall'applicazione per ricevere callback asincroni.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Enumera i dispositivi connessi al computer e fornisce un modo semplice per richiedere informazioni di installazione per il dispositivo, inclusi il produttore, il nome descrittivo e la descrizione.                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Leggere e scrivere le proprietà per un oggetto nel dispositivo.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Legge e scrive più proprietà su più oggetti in un dispositivo, in modo asincrono.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Implementata dall'applicazione per tenere traccia dello stato di avanzamento di un'operazione asincrona avviata tramite l'interfaccia **IPortableDevicePropertiesBulk** .                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Consente di accedere ai dati di un oggetto.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Solo Windows 7. Fornisce accesso di basso livello a un servizio di dispositivo portatile.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Solo Windows 7. Recupera un'ampia gamma di funzionalità di servizio, tra cui formati supportati, comandi, metodi e profili di rendering.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Solo Windows 7. Richiama i metodi in modo sincrono e asincrono in un servizio.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Solo Windows 7. Implementata dall'applicazione per tenere traccia del completamento di un'operazione asincrona di un metodo di servizio iniziata chiamando [ **IPortableDeviceServiceMethods:: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Solo Windows 7. Enumera i servizi supportati da un dispositivo e recupera il dispositivo associato a un servizio.                                                                                                             |



 

Il diagramma seguente illustra il modo in cui un'applicazione ottiene la maggior parte delle interfacce necessarie. Non vengono visualizzati tutti i metodi di tutte le interfacce o le interfacce implementate dall'applicazione.

![diagramma che illustra la creazione e il recupero delle interfacce client più richieste](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



