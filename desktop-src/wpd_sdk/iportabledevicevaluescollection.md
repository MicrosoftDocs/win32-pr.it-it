---
description: L'interfaccia IPortableDeviceValuesCollection include una raccolta di interfacce IPortableDeviceValues indicizzate in base zero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interfaccia IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324505"
---
# <a name="iportabledevicevaluescollection-interface"></a>Interfaccia IPortableDeviceValuesCollection

L'interfaccia **IPortableDeviceValuesCollection** include una raccolta di interfacce **IPortableDeviceValues** indicizzate in base zero. Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceValuesCollection**.

## <a name="members"></a>Membri

L'interfaccia **IPortableDeviceValuesCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValuesCollection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IPortableDeviceValuesCollection** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Aggiungere**](iportabledevicevaluescollection-add.md)           | Aggiunge un elemento alla raccolta<br/>                                           |
| [**Deselezionare**](iportabledevicevaluescollection-clear.md)       | Rilascia tutti gli elementi dall'insieme.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Recupera un elemento dalla raccolta in base a un indice in base zero.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Recupera il numero di elementi nella raccolta.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

