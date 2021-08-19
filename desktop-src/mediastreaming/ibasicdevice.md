---
title: Interfaccia IBasicDevice
description: Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API Streaming multimediale dell'interfaccia IBasicDevice
- Interfaccia IBasicDevice API Streaming multimediale , descritta
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25a60a3f722faac473b6f779de2d609cbdfc4ecb257d671136a8ef80535fdf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060361"
---
# <a name="ibasicdevice-interface"></a>Interfaccia IBasicDevice

Incapsula i metodi e gli eventi necessari per modellare un dispositivo DLNA.

## <a name="members"></a>Membri

**L'interfaccia IBasicDevice** eredita da [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **IBasicDevice** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IBasicDevice** include questi metodi.



| Metodo                                                                                 | Descrizione                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**aggiungere \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)       | Registra un gestore eventi per [**l'evento ConnectionStatusChanged.**](connectionstatuschanged.md)<br/>                |
| [**CanWakeDevices**](ibasicdevice-canwakedevices.md)                                  | Recupera un valore che indica se il dispositivo può essere riattivato.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Restituisce un valore di enumerazione che indica se il dispositivo è attualmente in linea, non in linea o in sospensione ma riattivabile.<br/> |
| [**Descrizione**](ibasicdevice-description.md)                                        | Recupera una descrizione del dispositivo.<br/>                                                                              |
| [**DiscoveredOnCurrentNetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | Recupera un valore che indica se il dispositivo si trova nella rete corrente.<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | Recupera il nome descrittivo del dispositivo.<br/>                                                                               |
| [**Icone**](ibasicdevice-icons.md)                                                    | Restituisce un vettore [**di interfacce IDeviceIcon.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                                  |
| [**Ipaddresses**](ibasicdevice-ipaddresses.md)                                        | Restituisce un vettore di indirizzi IP.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Recupera il nome del produttore del dispositivo.<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | Recupera l'URL del produttore del dispositivo.<br/>                                                                            |
| [**Modelname**](ibasicdevice-modelname.md)                                            | Recupera il nome del modello del dispositivo.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Recupera il numero di modello del dispositivo.<br/>                                                                                |
| [**ModelUrl**](ibasicdevice-modelurl.md)                                              | Recupera l'URL del modello del dispositivo.<br/>                                                                                   |
| [**PhysicalAddresses**](ibasicdevice-physicaladdresses.md)                            | Restituisce un vettore di indirizzi fisici.<br/>                                                                             |
| [**PresentationUrl**](ibasicdevice-presentationurl.md)                                | Recupera l'URL di presentazione del dispositivo.<br/>                                                                            |
| [**RemoteStreamingUrls**](ibasicdevice-remotestreamingurls.md)                        | Restituisce un vettore di URL di streaming remoto.<br/>                                                                          |
| [**rimuovere \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) | Annulla la registrazione di un gestore eventi per [**l'evento ConnectionStatusChanged.**](connectionstatuschanged.md)<br/>              |
| [**Serialnumber**](ibasicdevice-serialnumber.md)                                      | Recupera il numero di serie del dispositivo.<br/>                                                                               |
| [**Tipo**](ibasicdevice-type.md)                                                      | Recupera un valore di enumerazione che indica il tipo di dispositivo del dispositivo DLNA.<br/>                                       |
| [**UniqueDeviceName**](ibasicdevice-uniquedevicename.md)                              | Recupera il nome UDN (Unique Device Name) del dispositivo.<br/>                                                                    |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

