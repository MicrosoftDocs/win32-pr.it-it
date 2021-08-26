---
title: Interfaccia IMsRdpDevice
description: Contiene informazioni su un oggetto dispositivo.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDevice Servizi Desktop remoto
- Interfaccia IMsRdpDevice Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d545bebde1ed2df8a4c67cdf8d32d0a91499ed42076b2c1b31539d96069d3688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033091"
---
# <a name="imsrdpdevice-interface"></a>Interfaccia IMsRdpDevice

Contiene informazioni su un oggetto dispositivo.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpDevice** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDevice** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IMsRdpDevice** ha queste proprietà.



| Proprietà                                                               | Tipo di accesso           | Descrizione                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Sola lettura<br/>  | Recupera la descrizione del dispositivo da visualizzare all'utente se il nome visualizzato non è disponibile.<br/> |
| [**DeviceInstanceId**](imsrdpdevice-deviceinstanceid.md)<br/>   | Sola lettura<br/>  | Recupera l'identificatore dell'istanza del dispositivo.<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | Sola lettura<br/>  | Recupera il nome visualizzato per il dispositivo.<br/>                                                         |
| [**RedirectionState**](imsrdpdevice-redirectionstate.md)<br/>   | Lettura/Scrittura<br/> | Indica lo stato di reindirizzamento del dispositivo.<br/>                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice è definito come 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Connessione Web Desktop remoto di riferimento](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

