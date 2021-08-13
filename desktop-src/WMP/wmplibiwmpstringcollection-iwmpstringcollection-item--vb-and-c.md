---
title: Metodo IWMPStringCollection Item
description: Il metodo Item restituisce la stringa in corrispondenza dell'indice specificato.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Metodo Item Windows Media Player
- Metodo Item Windows Media Player, interfaccia IWMPStringCollection
- Interfaccia IWMPStringCollection Windows Media Player , metodo Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47928502dce9ed4deb12461763a499de5d962aa1303b4c9cc5eacb02c7619da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568427"
---
# <a name="iwmpstringcollectionitem-method"></a>Metodo IWMPStringCollection::Item

Il **metodo Item** restituisce la stringa in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lIndex* \[ Pollici\]
</dt> <dd>

Oggetto **System.Int32** che rappresenta l'indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.String** che rappresenta la stringa in corrispondenza dell'indice specificato.

## <a name="remarks"></a>Commenti

**L'interfaccia IWMPStringCollection** viene usata per recuperare il set di valori disponibili per un attributo. Ad esempio, il **metodo IWMPMediaCollection.getAttributeStringCollection** può essere usato per recuperare **un'interfaccia IWMPStringCollection** che rappresenta tutti i valori per l'attributo Genre all'interno del tipo di supporto Audio. Il **metodo Item** può quindi essere usato per scorrere tutti i valori possibili per l'attributo Genre.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPMediaCollection.getAttributeStringCollection (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





