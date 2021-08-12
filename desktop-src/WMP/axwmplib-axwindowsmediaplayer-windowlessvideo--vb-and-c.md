---
title: AxWindowsMediaPlayer.windowlessVideo - proprietà
description: La proprietà windowlessVideo ottiene o imposta un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Proprietà windowlessVideo Windows Media Player
- proprietà windowlessVideo Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , proprietà windowlessVideo
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
ms.openlocfilehash: 3a63a7246e730f73bd6d6f27111112a3db2029e3b53c80569e2e013771da6708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581521"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>AxWindowsMediaPlayer.windowlessVideo - proprietà

La proprietà windowlessVideo ottiene o imposta un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore System.Boolean che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra. Il valore predefinito è false.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un controllo Windows Media Player incorporato esegue il rendering del video nella relativa finestra all'interno dell'area client. Quando **windowlessVideo** è impostato su true, l'oggetto Windows Media Player esegue il rendering del video direttamente nell'area client, in modo che sia possibile applicare effetti speciali o applicare un livello al video con testo.

In Windows Vista il rendering di video in modalità senza finestra può ridurre le prestazioni.

Il recupero di un valore per questa proprietà non è supportato per Netscape Navigator. L'impostazione di un valore per questa proprietà Netscape Navigator risultati imprevisti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





