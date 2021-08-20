---
title: Metodo topMenu IWMPDVD
description: Il metodo topMenu arresta la riproduzione e visualizza il menu superiore (o radice) per il titolo corrente.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Metodo topMenu Windows Media Player
- Metodo topMenu Windows Media Player, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player metodo , topMenu
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f9cc1dcd528b93e9959f63a387747e510f7dd57b403ad70e41768d77006337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930213"
---
# <a name="iwmpdvdtopmenu-method"></a>Metodo IWMPDVD::topMenu

Il **metodo topMenu** arresta la riproduzione e visualizza il menu superiore (o radice) per il titolo corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Il DVD deve contenere un menu per il funzionamento di questo metodo. Alcuni DVD vengono creati in modo che i **metodi topMenu** e **IWMPDVD.titleMenu** abilitino lo stesso menu. Il **metodo topMenu** in genere richiama il menu principale (o radice), ma può richiamare il menu del titolo se non è disponibile alcun menu radice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.titleMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





