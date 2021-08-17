---
title: Proprietà Error di IWMPMedia2
description: La proprietà Error ottiene un'interfaccia IWMPErrorItem se l'elemento multimediale presenta una condizione di errore.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Errore - proprietà Windows Media Player
- Proprietà Error Windows Media Player, interfaccia IWMPMedia2
- Interfaccia IWMPMedia2 Windows Media Player , proprietà Error
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
ms.openlocfilehash: 6c841e52f2a5adda5a2098f591b141aa334ee5138c1a5cc7d6eff9b54dca5e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331971"
---
# <a name="iwmpmedia2error-property"></a>Proprietà IWMPMedia2::Error

La **proprietà Error** ottiene **un'interfaccia IWMPErrorItem** se l'elemento multimediale presenta una condizione di errore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Valore proprietà

Interfaccia **WMPLib.IWMPErrorItem** che fornisce l'accesso alle informazioni sulla condizione di errore.

## <a name="remarks"></a>Commenti

Se non è possibile riprodurre l'elemento multimediale, questa proprietà ottiene **un'interfaccia IWMPErrorItem** che contiene informazioni sul problema riscontrato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia2 (VB e C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





