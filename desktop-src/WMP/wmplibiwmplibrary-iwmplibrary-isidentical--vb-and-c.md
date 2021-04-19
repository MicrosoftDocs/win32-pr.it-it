---
title: Metodo IWMPLibrary identico
description: Il metodo IsValid restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- Metodo di Media Player di Windows identico
- Metodo identico Media Player Windows, interfaccia IWMPLibrary
- Interfaccia IWMPLibrary Windows Media Player, metodo identico
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
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332426"
---
# <a name="iwmplibraryisidentical-method"></a>Metodo IWMPLibrary:: IsValid

Il **Metodo IsValid** restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.

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

*pIWMPLibrary* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPLibrary** che rappresenta l'oggetto da confrontare con quello corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Boolean** che rappresenta il risultato del confronto. Il valore **true** indica che gli oggetti sono uguali.

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

 

 





