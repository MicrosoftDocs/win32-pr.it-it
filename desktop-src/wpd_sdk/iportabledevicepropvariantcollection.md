---
description: L'interfaccia IPortableDevicePropVariantCollection contiene una raccolta di valori PROPVARIANT indicizzati dello stesso VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interfaccia IPortableDevicePropVariantCollection (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f5f6a59dfd741eb524c4b6015c5384123b6a2d491b5bdc030053bbc88ad6800a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026889"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>Interfaccia IPortableDevicePropVariantCollection

**L'interfaccia IPortableDevicePropVariantCollection** contiene una raccolta di valori **PROPVARIANT** indicizzati dello stesso VARTYPE. VarTYPE del primo elemento aggiunto alla raccolta determina il VARTYPE della raccolta. Un tentativo di aggiungere un elemento di un VARTYPE diverso potrebbe non riuscire se il **valore PROPVARIANT** non può essere modificato nell'oggetto VARTYPE corrente della raccolta. Per modificare VARTYPE della raccolta, chiamare **ChangeType**.

Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDevicePropVariantCollection**.

## <a name="members"></a>Membri

**L'interfaccia IPortableDevicePropVariantCollection** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDevicePropVariantCollection** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IPortableDevicePropVariantCollection.**



| Metodo                                                                | Descrizione                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Aggiungere**](iportabledevicepropvariantcollection-add.md)               | Aggiunge un elemento alla raccolta.<br/>                                          |
| [**Changetype**](iportabledevicepropvariantcollection-changetype.md) | Converte tutti gli elementi nella raccolta nell'oggetto VARTYPE specificato.<br/>           |
| [**Cancella**](iportabledevicepropvariantcollection-clear.md)           | Libera e quindi rimuove tutti gli elementi dalla raccolta.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Recupera un elemento dalla raccolta in base a un indice in base zero.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Recupera il numero di elementi in questa raccolta.<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | Recupera il tipo di dati degli elementi nella raccolta.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

