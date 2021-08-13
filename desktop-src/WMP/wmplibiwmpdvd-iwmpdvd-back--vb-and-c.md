---
title: Metodo indietro IWMPDVD
description: Il metodo Indietro modifica la visualizzazione da un sottomenu al menu padre.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Metodo back Windows Media Player
- metodo back Windows Media Player, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player , metodo back
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
ms.openlocfilehash: 483e8e36f8ac5e539925306a53c04d144fb6de1281878840fc598c96c814f002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414561"
---
# <a name="iwmpdvdback-method"></a>Metodo IWMPDVD::back

Il **metodo Indietro** modifica la visualizzazione da un sottomenu al menu padre.

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

Ogni DVD viene creato in modo diverso. Alcuni DVD vengono creati in modo che il metodo sia disponibile dal menu radice, ma quando viene richiamato, non `back` esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





