---
title: Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer
description: L'evento ScriptCommand si verifica quando viene ricevuto un URL o un comando sincronizzato. | Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26724d8d2d86bd14be9aa5360678dd9caf54620e48d4b361ab120bc2b8927fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509331"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer

L'evento ScriptCommand si verifica quando viene ricevuto un URL o un comando sincronizzato.

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a>Dati eventi

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, che contiene le proprietà seguenti correlate a questo evento.



| Proprietà | Descrizione                                                   |
|----------|---------------------------------------------------------------|
| scType   | System.StringSpecifica il tipo di comando script.<br/> |
| param    | System.StringSpecifica il comando script.<br/>         |



 

## <a name="remarks"></a>Commenti

I comandi possono essere incorporati tra i suoni e le immagini di un Windows file o flusso multimediale. I comandi sono una coppia di stringhe Unicode associate a un'ora designata nel flusso. Quando il flusso raggiunge l'ora associata al comando, il controllo Windows Media Player invia un **evento ScriptCommand** con due parametri. Un parametro specifica il tipo di comando inviato e l'altro parametro specifica il comando. Il tipo di parametro viene usato per determinare la modalità di elaborazione del parametro del comando. Qualsiasi tipo di comando può essere incorporato in un file o in un flusso che deve essere gestito **dall'evento ScriptCommand.**

Nella tabella seguente sono elencati i tipi di comando script che vengono elaborati automaticamente da Windows Media Player.



| Tipo                   | Descrizione                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Il controllo visualizza il testo associato nell'elemento HTML specificato da IWMPClosedCaption. **captioningId**.                                                       |
| Evento                  | Il controllo esegue le istruzioni definite per l'evento specificato.                                                                                                  |
| Filename               | Il controllo reimposta la proprietà **URL,** tenta di aprire il file specificato e inizia a riprodurre immediatamente il nuovo flusso.                                        |
| OPENEVENT              | Buffer del comando di tipo EVENT associato per l'esecuzione temporale dello script EVENT.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Il *parametro param* contiene il testo del testo sincronizzato. Windows Media Player il testo del testo nell'area dei sottotitoli codificati della **funzionalità In** riproduzione. |
| TEXT                   | Il controllo visualizza il testo associato nell'elemento HTML specificato da IWMPClosedCaption. **captioningId**.                                                       |
| URL                    | Il controllo apre automaticamente l'URL specificato usando il browser Internet predefinito se IWMPSettings. **La proprietà invokeURLs** è impostata su true.                    |



 

È possibile incorporare qualsiasi altro tipo di comando, purché si fornirà il codice per gestire il comando. Anche se i comandi sconosciuti vengono ignorati dal controllo Windows Media Player, vengono comunque consegnati **all'evento ScriptCommand.**

L'evento ScriptCommand non viene chiamato se il file viene analizzato in modalità avanzamento rapido o riavvolgimento.

I comandi URL ricevuti dal controllo Windows Media Player vengono richiamati automaticamente nel Web browser se IWMPSettings. **La proprietà invokeURLs** è impostata su true. È possibile usare IWMPSettings. **proprietà defaultFrame** per specificare il frame di destinazione in cui viene visualizzata la pagina Web.

L'URL inviato Windows Media Player viene elaborato in relazione all'URL di base specificato da IWMPSettings. **proprietà baseURL.** L'URL di base viene concatenato all'URL relativo, con un URL completamente specificato che viene passato come parametro di comando **dall'evento ScriptCommand.**

Il Windows Media Player controllo elabora sempre i comandi URL in ingresso nel modo seguente:

1.  Viene ricevuto un comando di tipo URL.
2.  IWMPSettings. **baseURL** viene usato per creare un URL completo dall'URL relativo specificato nel comando script.
3.  **Viene chiamato ScriptCommand.**
4.  Al **termine di ScriptCommand,** IWMPSettings. **invokeURLs è** selezionato.
5.  Se IWMPSettings. **invokeURLs** è true e il comando è un comando URL. Viene richiamato l'URL specificato. Se IWMPSettings. **invokeURLs** è false oppure se il comando non è un comando URL, il comando viene ignorato.

Quando si crea un file Windows Media, è possibile specificare in quale frame viene visualizzato il nuovo URL concatenando due e commerciale e il nome del frame nel campo del parametro . L'esempio seguente illustra i tipici **parametri ScriptCommand.** Specifica che l'URL *mypage* deve essere avviato nel *frame myframe.*


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



L'evento ScriptCommand non viene chiamato se il file viene analizzato (inoltrato o ricaricato rapidamente).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.captioningId (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.baseURL (VB e C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.defaultFrame (VB e C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.invokeURLs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





