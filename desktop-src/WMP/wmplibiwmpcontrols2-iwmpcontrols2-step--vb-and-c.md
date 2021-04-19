---
title: Metodo IWMPControls2 Step
description: Il metodo Step fa passare l'elemento del supporto video corrente al frame successivo o al frame precedente e bloccare la riproduzione.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- Metodo Step Media Player Windows
- Metodo Step Media Player Windows, interfaccia IWMPControls2
- Interfaccia IWMPControls2 Windows Media Player, Metodo Step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332468"
---
# <a name="iwmpcontrols2step-method"></a>Metodo IWMPControls2:: Step

Il metodo **Step** fa passare l'elemento del supporto video corrente al frame successivo o al frame precedente e bloccare la riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*lStep* \[ in\]
</dt> <dd>

Valore **System. Int32** che indica il numero di frame da scorrere prima del blocco. Deve essere impostato su 1 o-1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo supporta attualmente solo i parametri 1 o-1, pertanto è possibile eseguire solo un passaggio di un frame alla volta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





