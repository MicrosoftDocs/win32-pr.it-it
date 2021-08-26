---
description: L'interfaccia IPortableDeviceValuesCollection contiene una raccolta di interfacce IPortableDeviceValues indicizzate in base zero.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interfaccia IPortableDeviceValuesCollection (PortableDeviceTypes.h)
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
ms.openlocfilehash: cd6547a96013b2b83ce9962a62f0837dd01cacac6f3e64adc3b964754c148c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928381"
---
# <a name="iportabledevicevaluescollection-interface"></a>Interfaccia IPortableDeviceValuesCollection

**L'interfaccia IPortableDeviceValuesCollection** contiene una raccolta di interfacce **IPortableDeviceValues** indicizzate in base zero. Questa interfaccia può essere recuperata da un metodo oppure, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceValuesCollection**.

## <a name="members"></a>Membri

**L'interfaccia IPortableDeviceValuesCollection** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceValuesCollection** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IPortableDeviceValuesCollection** include questi metodi.



| Metodo                                                       | Descrizione                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Aggiungere**](iportabledevicevaluescollection-add.md)           | Aggiunge un elemento alla raccolta<br/>                                           |
| [**Cancella**](iportabledevicevaluescollection-clear.md)       | Rilascia tutti gli elementi dalla raccolta.<br/>                                  |
| [**GetAt**](iportabledevicevaluescollection-getat.md)       | Recupera un elemento dalla raccolta in base a un indice in base zero.<br/>             |
| [**GetCount**](iportabledevicevaluescollection-getcount.md) | Recupera il numero di elementi nella raccolta.<br/>                         |
| [**RemoveAt**](iportabledevicevaluescollection-removeat.md) | Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

