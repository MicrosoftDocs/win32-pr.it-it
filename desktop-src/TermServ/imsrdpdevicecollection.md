---
title: Interfaccia IMsRdpDeviceCollection
description: Rappresenta una raccolta di oggetti dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5f7008b0b524150cd106b9bbe97d21a8de890773d8b0b461a6ae3045e847a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000741"
---
# <a name="imsrdpdevicecollection-interface"></a>Interfaccia IMsRdpDeviceCollection

Rappresenta una raccolta di oggetti dispositivo.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpDeviceCollection** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDeviceCollection** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IMsRdpDeviceCollection** include questi metodi.



| Metodo                                                        | Descrizione                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDevices**](imsrdpdevicecollection-rescandevices.md) | Aggiorna l'elenco di oggetti nella raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IMsRdpDeviceCollection** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**DeviceById**](imsrdpdevicecollection-devicebyid.md)<br/>       | Sola lettura<br/> | Recupera il dispositivo con l'identificatore specificato.<br/> |
| [**DeviceByIndex**](imsrdpdevicecollection-devicebyindex.md)<br/> | Sola lettura<br/> | Recupera il dispositivo in corrispondenza dell'indice specificato.<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | Sola lettura<br/> | Recupera il conteggio degli oggetti nella raccolta.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection è definito come 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Connessione Web Desktop remoto di riferimento](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

