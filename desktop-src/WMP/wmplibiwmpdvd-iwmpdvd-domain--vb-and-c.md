---
title: Proprietà di dominio IWMPDVD
description: La proprietà del dominio ottiene il dominio corrente del DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Proprietà del dominio Media Player Windows
- Proprietà del dominio Media Player Windows, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player, proprietà del dominio
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
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332449"
---
# <a name="iwmpdvddomain-property"></a>IWMPDVD::d proprietà ominio

La proprietà del **dominio** ottiene il dominio corrente del DVD.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che corrisponde a uno dei valori seguenti.



| Valore                                                                                        | Significato                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Esecuzione dell'inizializzazione predefinita di un disco DVD.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Visualizzazione dei menu per l'intero disco. Noto anche come menu di scelta rapida per Windows Media Player. Comunemente chiamato menu titolo o menu in alto.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Visualizzazione dei menu per il set di titoli corrente. Noto anche come titleMenu per Windows Media Player. Comunemente chiamato menu radice.<br/>          |
| <dl> <dt>title</dt> </dl>             | In genere, viene visualizzato il titolo corrente.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | Il navigatore DVD si trova nel dominio di arresto DVD.<br/>                                                                                          |
| <dl> <dt>non definito</dt> </dl>         | Windows Media Player non è in alcun dominio DVD.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Alcuni DVD non contengono i domini firstPlay, videoManagerMenu o videoTitleSetMenu.

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

 

 





