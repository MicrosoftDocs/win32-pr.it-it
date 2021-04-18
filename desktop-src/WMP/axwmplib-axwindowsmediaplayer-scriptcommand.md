---
title: Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer
description: L'evento ScriptCommand si verifica quando viene ricevuto un comando o un URL sincronizzato. | Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer Media Player Windows
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
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328309"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>Evento ScriptCommand dell'oggetto AxWindowsMediaPlayer

L'evento ScriptCommand si verifica quando viene ricevuto un comando o un URL sincronizzato.

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

Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_ScriptCommandEventHandler WMPOCXEvents**. Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, che contiene le seguenti proprietà correlate a questo evento.



| Proprietà | Descrizione                                                   |
|----------|---------------------------------------------------------------|
| scType   | System. StringSpecifies il tipo di comando per script.<br/> |
| param    | System. StringSpecifies il comando script.<br/>         |



 

## <a name="remarks"></a>Commenti

I comandi possono essere incorporati tra i suoni e le immagini di un file o di un flusso Windows Media. I comandi sono una coppia di stringhe Unicode associate a un'ora designata nel flusso. Quando il flusso raggiunge l'ora associata al comando, il controllo Windows Media Player invia un evento **ScriptCommand** con due parametri. Un parametro specifica il tipo di comando inviato e l'altro parametro specifica il comando. Il tipo di parametro viene utilizzato per determinare la modalità di elaborazione del parametro del comando. Qualsiasi tipo di comando può essere incorporato in un file o in un flusso che deve essere gestito dall'evento **ScriptCommand** .

Nella tabella seguente sono elencati i tipi di comando script elaborati automaticamente da Windows Media Player.



| Tipo                   | Descrizione                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Il controllo Visualizza il testo associato nell'elemento HTML specificato da IWMPClosedCaption. **captioningId**.                                                       |
| EVENTO                  | Il controllo esegue le istruzioni definite per l'evento specificato.                                                                                                  |
| FILENAME               | Il controllo Reimposta la proprietà **URL** , tenta di aprire il file specificato e inizia immediatamente a riprodurre il nuovo flusso.                                        |
| OPENEVENT              | Memorizza nel buffer il comando del tipo di evento associato per l'esecuzione tempestiva dello script di evento.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Il parametro *param* contiene il testo lirico sincronizzato. Windows Media Player Visualizza il testo lirico nell'area didascalia chiusa della funzionalità **ora di riproduzione** . |
| TEXT                   | Il controllo Visualizza il testo associato nell'elemento HTML specificato da IWMPClosedCaption. **captioningId**.                                                       |
| URL                    | Il controllo apre automaticamente l'URL specificato utilizzando il browser Internet predefinito, se IWMPSettings. la proprietà **invokeURLs** è impostata su true.                    |



 

È possibile incorporare qualsiasi altro tipo di comando purché si fornisca il codice per gestire il comando. Sebbene i comandi sconosciuti vengano ignorati dal controllo Media Player di Windows, vengono comunque passati all'evento **ScriptCommand** .

L'evento ScriptCommand non viene chiamato se il file viene sottoposta a scansione in modalità avanzamento rapido o riavvolgimento.

I comandi dell'URL ricevuti dal controllo Media Player di Windows vengono richiamati automaticamente nel Web browser predefinito, se IWMPSettings. la proprietà **invokeURLs** è impostata su true. È possibile usare IWMPSettings. proprietà **DefaultFrame** per specificare il frame di destinazione in cui viene visualizzata la pagina Web.

L'URL inviato a Windows Media Player viene elaborato in relazione all'URL di base specificato da IWMPSettings. proprietà **BaseUrl** . L'URL di base viene concatenato all'URL relativo, ottenendo un URL completo che viene passato come parametro Command dall'evento **ScriptCommand** .

Il controllo Media Player Windows elabora sempre i comandi URL in arrivo nel modo seguente:

1.  Viene ricevuto un comando di tipo URL.
2.  IWMPSettings. **BaseUrl** viene usato per creare un URL completo dall'URL relativo specificato nel comando script.
3.  Viene chiamato **ScriptCommand** .
4.  Dopo la restituzione di **ScriptCommand** , IWMPSettings. **invokeURLs** è selezionato.
5.  Se IWMPSettings. **invokeURLs** è true e il comando è un comando URL, viene richiamato l'URL specificato. Se IWMPSettings. **invokeURLs** è false o se il comando non è un comando URL, il comando viene ignorato.

Quando si crea un file di Windows Media, è possibile specificare il frame in cui viene visualizzato il nuovo URL concatenando due e commerciali e il nome del frame nel campo del parametro. Nell'esempio seguente vengono illustrati i tipici parametri **ScriptCommand** . Specifica che è necessario avviare la *pagina* URL *nel frame frame* .


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



L'evento ScriptCommand non viene chiamato se il file viene sottoposta a scansione (con avanzamento rapido o riavvolto).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. captioningId (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB e C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB e C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





