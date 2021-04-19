---
description: L'interfaccia IPortableDevicePropVariantCollection include una raccolta di valori PROPVARIANT indicizzati dello stesso VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Interfaccia IPortableDevicePropVariantCollection (PortableDeviceTypes. h)
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
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326693"
---
# <a name="iportabledevicepropvariantcollection-interface"></a>Interfaccia IPortableDevicePropVariantCollection

L'interfaccia **IPortableDevicePropVariantCollection** include una raccolta di valori **PROPVARIANT** indicizzati dello stesso VARTYPE. Il VARTYPE del primo elemento aggiunto alla raccolta determina il VARTYPE della raccolta. Un tentativo di aggiungere un elemento di un VARTYPE diverso potrebbe non riuscire se non è possibile modificare il valore **PROPVARIANT** nell'elemento VarType corrente della raccolta. Per modificare il VARTYPE della raccolta, chiamare **ChangeType**.

Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDevicePropVariantCollection**.

## <a name="members"></a>Membri

L'interfaccia **IPortableDevicePropVariantCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDevicePropVariantCollection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IPortableDevicePropVariantCollection** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Aggiungere**](iportabledevicepropvariantcollection-add.md)               | Aggiunge un elemento alla raccolta.<br/>                                          |
| [**ChangeType**](iportabledevicepropvariantcollection-changetype.md) | Converte tutti gli elementi della raccolta nell'oggetto VARTYPE specificato.<br/>           |
| [**Deselezionare**](iportabledevicepropvariantcollection-clear.md)           | Libera, quindi rimuove tutti gli elementi dalla raccolta.<br/>                  |
| [**GetAt**](iportabledevicepropvariantcollection-getat.md)           | Recupera un elemento dalla raccolta in base a un indice in base zero.<br/>             |
| [**GetCount**](iportabledevicepropvariantcollection-getcount.md)     | Recupera il numero di elementi in questa raccolta.<br/>                        |
| [**GetType**](iportabledevicepropvariantcollection-gettype.md)       | Recupera il tipo di dati degli elementi nella raccolta.<br/>                  |
| [**RemoveAt**](iportabledevicepropvariantcollection-removeat.md)     | Rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

