---
title: AxWindowsMediaPlayer.stretchToFit - proprietà
description: La proprietà stretchToFit ottiene o imposta un valore che indica se il video visualizzato dal controllo Windows Media Player si adatta automaticamente alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Proprietà stretchToFit Windows Media Player
- Proprietà stretchToFit Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , proprietà stretchToFit
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
ms.openlocfilehash: a3090889207e0631fbc2f35613398b4c979f4c907cfe240e9f0a7374c74b00b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581511"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>AxWindowsMediaPlayer.stretchToFit - proprietà

La proprietà stretchToFit ottiene o imposta un valore che indica se il video visualizzato dal controllo Windows Media Player si adatta automaticamente alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Valore proprietà

Valore System.Boolean che indica se il video verrà adattato alla finestra. Il valore predefinito è false.

## <a name="remarks"></a>Commenti

Quando **stretchToFit** è impostato su true, il controllo Windows Media Player mantiene le proporzioni originali del video. Se le proporzioni del video non corrispondono alle proporzioni della finestra video, è possibile che le aree della maschera nera vengano visualizzate nella parte superiore e inferiore o a sinistra e a destra dell'immagine video.

Questa proprietà si applica al controllo Windows Media Player solo quando è incorporato in una pagina Web.

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

 

 





