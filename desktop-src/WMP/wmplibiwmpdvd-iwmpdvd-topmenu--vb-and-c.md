---
title: Metodo IWMPDVD tomenu
description: Il metodo di menu di scelta rapida interrompe la riproduzione e visualizza il menu principale (o radice) per il titolo corrente.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Windows Media Player metodo di menu di scelta rapida
- Metodo di menu di scelta rapida Windows Media Player, interfaccia IWMPDVD
- Interfaccia IWMPDVD Media Player Windows, metodo tomenu
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
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332446"
---
# <a name="iwmpdvdtopmenu-method"></a>Metodo IWMPDVD:: tomenu

Il metodo di **menu di scelta rapida** interrompe la riproduzione e visualizza il menu principale (o radice) per il titolo corrente.

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

Ogni DVD viene creato in modo diverso. Il DVD deve contenere un menu per il funzionamento di questo metodo. Alcuni DVD vengono creati in modo che i metodi **tomenu** e **IWMPDVD. titleMenu** aprano lo stesso menu. Il metodo di **menu di scelta rapida** richiama in genere il menu principale (o radice), ma può richiamare il menu del titolo se non è disponibile alcun menu radice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





