---
title: Metodo isIdentical IWMPLibrary
description: Il metodo isIdentical restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- Metodo isIdentical Windows Media Player
- Metodo isIdentical Windows Media Player, interfaccia IWMPLibrary
- Interfaccia IWMPLibrary Windows Media Player , metodo isIdentical
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ed37725bbda5b170ece8ce71c12499b42f0b361cbac3bbe65f1b875af06fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506051"
---
# <a name="iwmplibraryisidentical-method"></a>Metodo IWMPLibrary::isIdentical

Il **metodo isIdentical** restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pIWMPLibrary* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPLibrary** che rappresenta l'oggetto da confrontare con quello corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System.Boolean** che rappresenta il risultato del confronto. Il valore **true** indica che gli oggetti sono uguali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





