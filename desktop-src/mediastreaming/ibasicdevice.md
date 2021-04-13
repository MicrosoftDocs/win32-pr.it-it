---
title: Interfaccia IBasicDevice
description: Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API di streaming multimediale dell'interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, descritta
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399915"
---
# <a name="ibasicdevice-interface"></a>Interfaccia IBasicDevice

Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.

## <a name="members"></a>Membri

L'interfaccia **IBasicDevice** eredita da [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **IBasicDevice** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IBasicDevice** dispone di questi metodi.



| Metodo                                                                                 | Descrizione                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungi \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)       | Registra un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>                |
| [**CanWakeDevices**](ibasicdevice-canwakedevices.md)                                  | Recupera un valore che indica se il dispositivo può essere riattivato.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Restituisce un valore di enumerazione che indica se il dispositivo è attualmente in linea, non in linea o in sospensione ma riattivabile.<br/> |
| [**Descrizione**](ibasicdevice-description.md)                                        | Recupera una descrizione del dispositivo.<br/>                                                                              |
| [**DiscoveredOnCurrentNetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | Recupera un valore che indica se il dispositivo si trova nella rete corrente.<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | Recupera il nome descrittivo del dispositivo.<br/>                                                                               |
| [**Icone**](ibasicdevice-icons.md)                                                    | Restituisce un vettore di interfacce [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .<br/>                                                  |
| [**IpAddresses**](ibasicdevice-ipaddresses.md)                                        | Restituisce un vettore di indirizzi IP.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Recupera il nome del produttore del dispositivo.<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | Recupera l'URL del produttore del dispositivo.<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | Recupera il nome del modello del dispositivo.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Recupera il numero di modello del dispositivo.<br/>                                                                                |
| [**ModelUrl**](ibasicdevice-modelurl.md)                                              | Recupera l'URL del modello del dispositivo.<br/>                                                                                   |
| [**PhysicalAddresses**](ibasicdevice-physicaladdresses.md)                            | Restituisce un vettore di indirizzi fisici.<br/>                                                                             |
| [**PresentationUrl**](ibasicdevice-presentationurl.md)                                | Recupera l'URL di presentazione del dispositivo.<br/>                                                                            |
| [**RemoteStreamingUrls**](ibasicdevice-remotestreamingurls.md)                        | Restituisce un vettore di URL di streaming remoto.<br/>                                                                          |
| [**rimuovere \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) | Annulla la registrazione di un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>              |
| [**SerialNumber**](ibasicdevice-serialnumber.md)                                      | Recupera il numero di serie del dispositivo.<br/>                                                                               |
| [**Tipo**](ibasicdevice-type.md)                                                      | Recupera un valore di enumerazione che indica il tipo di dispositivo del dispositivo DLNA.<br/>                                       |
| [**UniqueDeviceName**](ibasicdevice-uniquedevicename.md)                              | Recupera il nome del dispositivo univoco del dispositivo (UDN).<br/>                                                                    |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

