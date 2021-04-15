---
title: Interfaccia IMsRdpDeviceCollection
description: Rappresenta una raccolta di oggetti dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto, descritta
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
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400236"
---
# <a name="imsrdpdevicecollection-interface"></a>Interfaccia IMsRdpDeviceCollection

Rappresenta una raccolta di oggetti dispositivo.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpDeviceCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDeviceCollection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpDeviceCollection** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDevices**](imsrdpdevicecollection-rescandevices.md) | Aggiorna l'elenco di oggetti nella raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpDeviceCollection** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**DeviceById**](imsrdpdevicecollection-devicebyid.md)<br/>       | Sola lettura<br/> | Recupera il dispositivo con l'identificatore specificato.<br/> |
| [**DeviceByIndex**](imsrdpdevicecollection-devicebyindex.md)<br/> | Sola lettura<br/> | Recupera il dispositivo in corrispondenza dell'indice specificato.<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | Sola lettura<br/> | Recupera il numero di oggetti nella raccolta.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection è definito come 56540617-D281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

