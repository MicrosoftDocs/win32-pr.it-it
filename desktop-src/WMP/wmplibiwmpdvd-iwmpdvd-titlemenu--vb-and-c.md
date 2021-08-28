---
title: Metodo titleMenu IWMPDVD
description: Il metodo titleMenu arresta la riproduzione e visualizza il menu del titolo.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- Metodo titleMenu Windows Media Player
- Metodo titleMenu Windows Media Player, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player, metodo titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff485cd09915ec9acb076d2c06a8aa28c3549bf6527495e5e32d4a01d483285a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000461"
---
# <a name="iwmpdvdtitlemenu-method"></a>Metodo IWMPDVD::titleMenu

Il **metodo titleMenu** arresta la riproduzione e visualizza il menu del titolo.

## <a name="syntax"></a>Sintassi


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Il DVD deve contenere un menu per il funzionamento di questo metodo. Alcuni DVD vengono creati in modo che i metodi **IWMPDVD.topMenu** e **titleMenu** abilitino lo stesso menu. Il **metodo titleMenu** in genere richiama il menu del titolo, ma può richiamare il menu in alto se non è disponibile alcun menu titolo.

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

[**IWMPDVD.topMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





