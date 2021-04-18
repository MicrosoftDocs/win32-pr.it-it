---
title: Metodo IWMPStringCollection2 identico
description: Il metodo IsValid restituisce un valore che indica se l'oggetto rappresentato dall'interfaccia fornita è identico a quello corrente.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- Metodo di Media Player di Windows identico
- Metodo identico Media Player Windows, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player, metodo identico
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331725"
---
# <a name="iwmpstringcollection2isidentical-method"></a>Metodo IWMPStringCollection2:: IsValid

Il **Metodo IsValid** restituisce un valore che indica se l'oggetto rappresentato dall'interfaccia fornita è identico a quello corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pIWMPStringCollection2* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPStringCollection2** che rappresenta l'oggetto da confrontare con quello corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Boolean** che rappresenta il risultato del confronto. Il valore **true** indica che gli oggetti della raccolta di stringhe sono uguali.

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPStringCollection2 (VB e C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





