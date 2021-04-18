---
title: Proprietà errore IWMPMedia2
description: La proprietà Error ottiene un'interfaccia IWMPErrorItem se l'elemento multimediale presenta una condizione di errore.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Finestra Proprietà errore Media Player
- Proprietà Error Media Player Windows, interfaccia IWMPMedia2
- Interfaccia IWMPMedia2 Windows Media Player, proprietà Error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324376"
---
# <a name="iwmpmedia2error-property"></a>Proprietà IWMPMedia2:: Error

La proprietà **Error** ottiene un'interfaccia **IWMPErrorItem** se l'elemento multimediale presenta una condizione di errore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Valore proprietà

Interfaccia **wmplib. IWMPErrorItem** che consente di accedere alle informazioni sulla condizione di errore.

## <a name="remarks"></a>Commenti

Se non è possibile riprodurre l'elemento multimediale, questa proprietà ottiene un'interfaccia **IWMPErrorItem** contenente informazioni sul problema riscontrato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia2 (VB e C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





