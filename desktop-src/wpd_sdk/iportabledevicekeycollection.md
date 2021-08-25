---
description: L'interfaccia IPortableDeviceKeyCollection contiene una raccolta di valori PROPERTYKEY. Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare CoCreate con CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interfaccia IPortableDeviceKeyCollection (PortableDeviceTypes.h)
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
ms.openlocfilehash: 0f648020ddb82db2a619f75bb125e94c7679f8dd3061ac282fcc0f911a498a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839391"
---
# <a name="iportabledevicekeycollection-interface"></a>Interfaccia IPortableDeviceKeyCollection

**L'interfaccia IPortableDeviceKeyCollection** contiene una raccolta di **valori PROPERTYKEY.** Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceKeyCollection.**

## <a name="members"></a>Membri

**L'interfaccia IPortableDeviceKeyCollection** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceKeyCollection** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IPortableDeviceKeyCollection.**



| Metodo                                                    | Descrizione                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Aggiungere**](iportabledevicekeycollection-add.md)           | Aggiunge una chiave di proprietà alla raccolta.<br/>                                   |
| [**Cancella**](iportabledevicekeycollection-clear.md)       | Elimina tutti gli elementi dalla raccolta.<br/>                                   |
| [**GetAt**](iportabledevicekeycollection-getat.md)       | Recupera un **elemento PROPERTYKEY** dalla raccolta in base all'indice.<br/>                |
| [**GetCount**](iportabledevicekeycollection-getcount.md) | Recupera il numero di chiavi in questa raccolta.<br/>                         |
| [**RemoveAt**](iportabledevicekeycollection-removeat.md) | Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

