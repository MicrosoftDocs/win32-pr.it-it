---
title: Proprietà di dominio IWMPDVD
description: La proprietà domain ottiene il dominio corrente del DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- proprietà di dominio Windows Media Player
- proprietà di dominio Windows Media Player, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player , proprietà di dominio
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b5f382d7c1db820905b45b924105225c0c5b55a569f85707e4e9f729e59596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000471"
---
# <a name="iwmpdvddomain-property"></a>Proprietà IWMPDVD::d omain

La **proprietà** domain ottiene il dominio corrente del DVD.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String** che è uno dei valori seguenti.



| Valore                                                                                        | Significato                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Esecuzione dell'inizializzazione predefinita di un disco DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Visualizzazione dei menu per l'intero disco. Noto anche come topMenu per Windows Media Player. Comunemente chiamato menu del titolo o menu superiore.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Visualizzazione dei menu per il set di titoli corrente. Noto anche come titleMenu per Windows Media Player. Comunemente chiamato menu radice.<br/>          |
| <dl> <dt>title</dt> </dl>             | In genere, visualizzando il titolo corrente.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | Lo strumento di spostamento DVD si trova nel dominio DVD Stop.<br/>                                                                                          |
| <dl> <dt>Indefinito</dt> </dl>         | Windows Media Player non si trova in alcun dominio DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Alcuni DVD non contengono i domini firstPlay, videoManagerMenu o videoTitleSetMenu.

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

 

 





