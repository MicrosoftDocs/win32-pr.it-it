---
description: L'interfaccia IPortableDeviceKeyCollection include una raccolta di valori PROPERTYKEY. Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare CoCreate con CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interfaccia IPortableDeviceKeyCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329894"
---
# <a name="iportabledevicekeycollection-interface"></a>Interfaccia IPortableDeviceKeyCollection

L'interfaccia **IPortableDeviceKeyCollection** include una raccolta di valori **PropertyKey** . Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceKeyCollection**.

## <a name="members"></a>Membri

L'interfaccia **IPortableDeviceKeyCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceKeyCollection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IPortableDeviceKeyCollection** dispone di questi metodi.



| Metodo                                                    | Descrizione                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Aggiungere**](iportabledevicekeycollection-add.md)           | Aggiunge una chiave di proprietà alla raccolta.<br/>                                   |
| [**Deselezionare**](iportabledevicekeycollection-clear.md)       | Elimina tutti gli elementi dall'insieme.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Recupera un **PropertyKey** dalla raccolta in base all'indice.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Recupera il numero di chiavi nella raccolta.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

