---
title: Impostazioni. avvio automatico
description: La proprietà AutoStart specifica o recupera un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Impostazioni. avvio automatico di Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325139"
---
# <a name="settingsautostart"></a>Impostazioni. avvio automatico

La proprietà **autostart** specifica o recupera un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.

## <a name="syntax"></a>Sintassi

Player. Settings. autostart

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                         |
|-------|---------------------------------------------------------------------|
| true  | Valore predefinito. L'elemento multimediale inizia la riproduzione automatica (vedere la sezione Osservazioni). |
| false | L'elemento multimediale non inizia la riproduzione automatica.                |



 

## <a name="remarks"></a>Commenti

Se **autostart** è impostato su true, l'elemento multimediale inizierà a riprodurre quando il *lettore*. **URL**, *Player*. **currentPlaylist** o *Player*. **currentMedia** è impostato. In caso contrario, non verrà avviata la riproduzione fino ai *controlli*. viene chiamato il metodo **Play** .

Poiché la proprietà di **avvio automatico** per la modalità completa di Windows Media Player può essere impostata a livello globale da eventi esterni (ad esempio il caricamento di un CD), non esiste alcun valore predefinito affidabile per le interfacce e i controlli del lettore remoto. Questo perché il motore di riproduzione del lettore in modalità completa viene usato in entrambi i casi.

È necessario impostare **avvio automatico** su false immediatamente prima di impostare *Player*. **URL**, *Player*. **currentPlaylist** o *Player*. **currentMedia** in interfacce e finestre Remote Media Player controlla se si desidera assicurarsi che la riproduzione dell'elemento multimediale non venga avviata immediatamente. Inoltre, a meno che non si imposti l' **avvio automatico** su true immediatamente prima di specificare un elemento multimediale, è consigliabile non fare affidamento su questa impostazione come sostituto per l'utilizzo dei *controlli*. metodo **Play** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento CHECKBOX HTML che consente all'utente di specificare se il controllo Player riproduce automaticamente l'elemento multimediale corrente. L'oggetto **Player** è stato creato con ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 





