---
title: Proprietà AxWindowsMediaPlayer. windowlessVideo
description: La proprietà windowlessVideo Ottiene o imposta un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Finestra delle proprietà di windowlessVideo Media Player
- Proprietà windowlessVideo Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333771"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>Proprietà AxWindowsMediaPlayer. windowlessVideo

La proprietà windowlessVideo Ottiene o imposta un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore System. Boolean che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra. Il valore predefinito è false.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un controllo di Windows Media Player incorporato esegue il rendering dei video nella propria finestra all'interno dell'area client. Quando **windowlessVideo** è impostato su true, l'oggetto Windows Media Player esegue il rendering del video direttamente nell'area client, in modo che sia possibile applicare effetti speciali o sovrapporre il video con il testo.

In Windows Vista, il rendering di video in modalità senza finestra può compromettere le prestazioni.

Il recupero di un valore per questa proprietà non è supportato per Netscape Navigator. L'impostazione di un valore per questa proprietà in Netscape Navigator può produrre risultati imprevisti.

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

 

 





