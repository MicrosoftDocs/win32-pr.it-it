---
title: THEME.playSound
description: Il metodo playSound riproduce il file audio specificato.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- THEME.playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9e6ac0cb7bdf4f8951bafbc89a0a41bf368afcd1021666eb7875739d1cd912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001751"
---
# <a name="themeplaysound"></a>THEME.playSound

Il **metodo playSound** riproduce il file audio specificato.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

Valore **String** che specifica il nome del file audio da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo consente di aggiungere effetti sonori a un'interfaccia, ad esempio quando si fa clic sui pulsanti. Il suono viene riprodotto direttamente dal sistema operativo e non Windows Media Player. Ciò significa che il suono non può essere controllato Windows Media Player impostazioni e metodi, ma può essere riprodotto mentre Windows Media Player un altro file multimediale digitale.

Questo metodo supporta solo i file WAV.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





