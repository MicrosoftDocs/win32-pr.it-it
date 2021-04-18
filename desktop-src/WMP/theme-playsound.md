---
title: THEME. playSound
description: Il metodo playSound riproduce il file audio specificato.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- THEME. playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328389"
---
# <a name="themeplaysound"></a>THEME. playSound

Il metodo **PlaySound** riproduce il file audio specificato.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

**Stringa** che specifica il nome del file audio da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo consente di aggiungere effetti acustici a un'interfaccia, ad esempio quando si fa clic sui pulsanti. Il suono viene riprodotto direttamente dal sistema operativo e non da Windows Media Player. Ciò significa che non è possibile controllare il suono con le impostazioni e i metodi Media Player di Windows, ma può essere riprodotto mentre Windows Media Player sta eseguendo un altro file multimediale digitale.

Questo metodo supporta solo file WAV.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





