---
title: Interfaccia IMsRdpDeviceV2
description: Contiene informazioni su un oggetto dispositivo. Si tratta di un miglioramento dell'interfaccia IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto , descritta
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
ms.openlocfilehash: cca125024592851b260fb8e4c1f43c7621d4897fec0fc19dfc80d18278e09cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000751"
---
# <a name="imsrdpdevicev2-interface"></a>Interfaccia IMsRdpDeviceV2

Contiene informazioni su un oggetto dispositivo. Si tratta di un miglioramento [**dell'interfaccia IMsRdpDevice.**](imsrdpdevice.md)

## <a name="members"></a>Membri

**L'interfaccia IMsRdpDeviceV2** eredita da [**IMsRdpDevice.**](imsrdpdevice.md) **IMsRdpDeviceV2** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IMsRdpDeviceV2** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Sola lettura<br/> | Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.<br/>                     |
| [**Istanza del dispositivo cmdevice**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Sola lettura<br/> | Contiene l'istanza del dispositivo di Configuration Manager del dispositivo.<br/>                       |
| [**Testo dispositivo**](imsrdpdevicev2-devicetext.md)<br/>               | Sola lettura<br/> | Contiene il testo del dispositivo.<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Sola lettura<br/> | Contiene un campo di bit che rappresenta una mappa di lettere di unità contenute nel dispositivo.<br/> |
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



 

 





