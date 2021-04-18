---
title: Interfaccia IMsRdpDevice
description: Contiene informazioni su un oggetto dispositivo.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDevice Servizi Desktop remoto
- Interfaccia IMsRdpDevice Servizi Desktop remoto, descritta
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
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301214"
---
# <a name="imsrdpdevice-interface"></a>Interfaccia IMsRdpDevice

Contiene informazioni su un oggetto dispositivo.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpDevice** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDevice** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpDevice** ha queste proprietà.



| Proprietà                                                               | Tipo di accesso           | Descrizione                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Sola lettura<br/>  | Recupera la descrizione del dispositivo da visualizzare all'utente se il nome visualizzato non è disponibile.<br/> |
| [**DeviceInstanceId**](imsrdpdevice-deviceinstanceid.md)<br/>   | Sola lettura<br/>  | Recupera l'identificatore dell'istanza del dispositivo.<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | Sola lettura<br/>  | Recupera il nome visualizzato per il dispositivo.<br/>                                                         |
| [**RedirectionState**](imsrdpdevice-redirectionstate.md)<br/>   | Lettura/Scrittura<br/> | Indica lo stato del reindirizzamento del dispositivo.<br/>                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice è definito come 60c3b9c8-9E92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

