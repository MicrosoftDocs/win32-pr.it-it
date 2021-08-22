---
description: Interfacce client
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Interfacce client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b44db8fdd42b20fb2ff7a3224bccf5214147069baa9187facdb1c832c375a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590396"
---
# <a name="client-interfaces"></a>Interfacce client

Le applicazioni usano i metodi supportati dalle interfacce seguenti per eseguire operazioni su dispositivi portatili. Queste operazioni includono l'apertura di una connessione a un dispositivo, il recupero di dati da un dispositivo, la scrittura di dati in un dispositivo e così via.



| Interfaccia                                                                              | Descrizione                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Enumera gli oggetti in un dispositivo portatile.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Fornisce l'accesso di basso livello a un dispositivo portatile.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Recupera un'ampia gamma di funzionalità del dispositivo, inclusi i formati supportati, i comandi e gli oggetti funzionali.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Fornisce metodi per creare, enumerare ed eliminare contenuto in un dispositivo.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Espone metodi aggiuntivi su un **IStream utilizzato** per i trasferimenti di dati.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Implementato dall'applicazione per ricevere callback asincroni.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Enumera i dispositivi connessi al computer e fornisce un modo semplice per richiedere informazioni di installazione per il dispositivo (inclusi produttore, nome descrittivo e descrizione).                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Leggere e scrivere proprietà per un oggetto nel dispositivo.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Legge e scrive più proprietà in più oggetti in un dispositivo, in modo asincrono.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Implementato dall'applicazione per tenere traccia dello stato di avanzamento di un'operazione asincrona avviata tramite **l'interfaccia IPortableDevicePropertiesBulk.**                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Fornisce l'accesso ai dati di un oggetto.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Windows solo 7. Fornisce l'accesso di basso livello a un servizio di dispositivo portatile.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Windows solo 7. Recupera un'ampia gamma di funzionalità del servizio, inclusi i formati supportati, i comandi, i metodi e i profili di rendering.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Windows solo 7. Richiama i metodi in modo sincrono e asincrono in un servizio.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Windows solo 7. Implementato dall'applicazione per tenere traccia del completamento di un'operazione asincrona del metodo del servizio avviata chiamando [ **IPortableDeviceServiceMethods::InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Windows solo 7. Enumera i servizi supportati da un dispositivo e recupera il dispositivo associato a un servizio.                                                                                                             |



 

Il diagramma seguente illustra come un'applicazione ottiene la maggior parte delle interfacce necessarie. Non vengono visualizzati tutti i metodi di tutte le interfacce o le interfacce implementate dall'applicazione.

![Diagramma che illustra la creazione e il recupero della maggior parte delle interfacce client necessarie](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



