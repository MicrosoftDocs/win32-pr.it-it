---
title: Interfaccia IMsRdpDeviceV2
description: Contiene informazioni su un oggetto dispositivo. Si tratta di un miglioramento dell'interfaccia IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300988"
---
# <a name="imsrdpdevicev2-interface"></a>Interfaccia IMsRdpDeviceV2

Contiene informazioni su un oggetto dispositivo. Si tratta di un miglioramento dell'interfaccia [**IMsRdpDevice**](imsrdpdevice.md) .

## <a name="members"></a>Membri

L'interfaccia **IMsRdpDeviceV2** eredita da [**IMsRdpDevice**](imsrdpdevice.md). **IMsRdpDeviceV2** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpDeviceV2** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Sola lettura<br/> | Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.<br/>                     |
| [**CmDeviceInstance**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Sola lettura<br/> | Contiene l'istanza del dispositivo di Configuration Manager del dispositivo.<br/>                       |
| [**DeviceText**](imsrdpdevicev2-devicetext.md)<br/>               | Sola lettura<br/> | Contiene il testo del dispositivo.<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Sola lettura<br/> | Contiene un bit che rappresenta una mappa delle lettere di unità contenute all'interno del dispositivo.<br/> |
| [**IsCompositeDevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | Sola lettura<br/> | Specifica se il dispositivo è un dispositivo composito.<br/>                                          |
| [**IsOptionalDevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Sola lettura<br/> | Specifica se il dispositivo è facoltativo per il reindirizzamento USB.<br/>                                |
| [**IsUSBDevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | Sola lettura<br/> | Specifica se il dispositivo è per il reindirizzamento USB.<br/>                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 con SP1<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2 con SP1<br/>                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



 

 





