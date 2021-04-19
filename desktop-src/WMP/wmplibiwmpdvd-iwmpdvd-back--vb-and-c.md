---
title: Metodo IWMPDVD back
description: Il metodo back modifica la visualizzazione da un sottomenu al relativo menu padre.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Back metodo Windows Media Player
- Metodo back Media Player Windows, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player, metodo back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332450"
---
# <a name="iwmpdvdback-method"></a>Metodo IWMPDVD:: back

Il metodo **back** modifica la visualizzazione da un sottomenu al relativo menu padre.

## <a name="syntax"></a>Sintassi


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Alcuni DVD vengono creati in modo che il `back` metodo sia disponibile dal menu radice, ma quando viene richiamato, non eseguirà alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





