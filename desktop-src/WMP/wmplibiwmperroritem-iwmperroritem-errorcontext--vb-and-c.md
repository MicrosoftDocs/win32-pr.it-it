---
title: Proprietà errorContext IWMPErrorItem
description: La proprietà errorContext ottiene un valore che indica il contesto dell'errore.
ms.assetid: e9ebd636-e611-49c6-9533-a02ff74db7bc
keywords:
- Proprietà errorContext Windows Media Player
- Proprietà errorContext Windows Media Player, interfaccia IWMPErrorItem
- Interfaccia IWMPErrorItem Windows Media Player , proprietà errorContext
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorContext
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60320df74d139e1cba3802c664ebff96e4531f569cd3321ae8821fc89ea5b0fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053649"
---
# <a name="iwmperroritemerrorcontext-property"></a>Proprietà IWMPErrorItem::errorContext

La **proprietà errorContext** ottiene un valore che indica il contesto dell'errore.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Object errorContext {get; set;}
```


```VB

Public ReadOnly Property errorContext As System.Object
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Object** che rappresenta il contesto di errore.

## <a name="remarks"></a>Commenti

Il contesto dell'errore è un'informazione usata da Microsoft per fornire informazioni aggiuntive al personale di supporto tecnico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





