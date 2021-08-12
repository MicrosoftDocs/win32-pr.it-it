---
title: Interfaccia IWMPControls2 (VB e C) (Wmp.h)
description: Fornisce un metodo che integra l'interfaccia IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- Interfaccia IWMPControls2 (VB e C) Windows Media Player
- Interfaccia IWMPControls2 (VB e C) Windows Media Player , descritta
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9757471526eb385168a10c505254b5a418ea7f9811576de95266c06817c73109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575921"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>Interfaccia IWMPControls2 (VB e C#)

Fornisce un metodo che integra [**l'interfaccia IWMPControls.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)

## <a name="members"></a>Membri

**L'interfaccia IWMPControls2 (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMPControls2 (VB e C#)** ha questi metodi.



| Metodo                                                           | Descrizione                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Passo**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Sposta l'elemento multimediale video corrente sul fotogramma successivo o sul fotogramma precedente e blocca la riproduzione.<br/> |



 

Il codice di esempio seguente illustra come accedere a [**un'interfaccia IWMPControls2.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) Il codice di esempio esegue il cast del valore [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) restituito dalla proprietà [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) a **un valore IWMPControls2.**

Per **C#**:


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



Per **VB**:


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





