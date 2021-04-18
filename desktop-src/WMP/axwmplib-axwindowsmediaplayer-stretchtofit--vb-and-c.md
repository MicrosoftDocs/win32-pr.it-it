---
title: Proprietà AxWindowsMediaPlayer. stretchToFit
description: La proprietà stretchToFit Ottiene o imposta un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Finestra delle proprietà di stretchToFit Media Player
- Proprietà stretchToFit Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330363"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>Proprietà AxWindowsMediaPlayer. stretchToFit

La proprietà stretchToFit Ottiene o imposta un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore System. Boolean che indica se il video si estenderà per adattarsi alla finestra. Il valore predefinito è false.

## <a name="remarks"></a>Commenti

Quando **stretchToFit** è impostato su true, il controllo Media Player Windows mantiene le proporzioni originali del video. Se le proporzioni del video non corrispondono alle proporzioni della finestra video, le aree della maschera nera possono essere visualizzate nella parte superiore e inferiore, o a sinistra e a destra, dell'immagine del video.

Questa proprietà si applica al controllo Media Player Windows solo se è incorporata in una pagina Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





