---
title: Metodo isIdentical IWMPStringCollection2
description: Il metodo isIdentical restituisce un valore che indica se l'oggetto rappresentato dall'interfaccia fornita è uguale a quello corrente.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- Metodo isIdentical Windows Media Player
- Metodo isIdentical Windows Media Player, interfaccia IWMPStringCollection2
- Interfaccia IWMPStringCollection2 Windows Media Player , metodo isIdentical
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
ms.openlocfilehash: 4576522c1b6d6834ded5e100a2618dcb45204f887420968a5828fdc5c9bd0fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330905"
---
# <a name="iwmpstringcollection2isidentical-method"></a>Metodo IWMPStringCollection2::isIdentical

Il **metodo isIdentical** restituisce un valore che indica se l'oggetto rappresentato dall'interfaccia fornita è uguale a quello corrente.

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

*pIWMPStringCollection2* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPStringCollection2** che rappresenta l'oggetto da confrontare con quello corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System.Boolean** che rappresenta il risultato del confronto. Il valore **true indica** che gli oggetti della raccolta di stringhe sono uguali.

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

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

 

 





