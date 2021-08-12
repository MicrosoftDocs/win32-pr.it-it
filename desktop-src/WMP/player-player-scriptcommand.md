---
title: Evento Player.ScriptCommand
description: L'evento ScriptCommand si verifica quando viene ricevuto un URL o un comando sincronizzato. | Evento Player.ScriptCommand
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Eventi ScriptCommand Windows Media Player
- ScriptCommand event Windows Media Player , Player class
- Classe Player Windows Media Player , evento ScriptCommand
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f54aac54cf56e65b71dbd604d57d5ae9404a0148db139779ced3aa9e0da0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572429"
---
# <a name="playerscriptcommand-event"></a>Evento Player.ScriptCommand

**L'evento ScriptCommand** si verifica quando viene ricevuto un URL o un comando sincronizzato.

## <a name="syntax"></a>Sintassi


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*scType* 
</dt> <dd>

Stringa che specifica il tipo di comando script.

</dd> <dt>

*Param* 
</dt> <dd>

**Stringa** che specifica il comando script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

I comandi possono essere incorporati tra i suoni e le immagini di un Windows file o flusso multimediale. I comandi sono una coppia di stringhe Unicode associate a un'ora designata nel flusso. Quando il flusso raggiunge l'ora associata al comando, il controllo Windows Media Player invia un evento **ScriptCommand** con due parametri. Un parametro specifica il tipo di comando inviato e l'altro parametro specifica il comando. Il tipo di parametro viene usato per determinare la modalità di elaborazione del parametro del comando. Qualsiasi tipo di comando può essere incorporato in un file o in un flusso che deve essere gestito **dall'evento ScriptCommand.**

Nella tabella seguente sono elencati i tipi di comando script che vengono elaborati automaticamente da Windows Media Player.



| Tipo                   | Descrizione                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Il controllo visualizza il testo associato nel div specificato da *ClosedCaption.* **captioningID**.                                                                  |
| Evento                  | Indica al controllo di eseguire le istruzioni definite per l'evento specificato.                                                                                          |
| Filename               | Il controllo reimposta la proprietà **URL,** tenta di aprire il file specificato e inizia a riprodurre immediatamente il nuovo flusso.                                        |
| OPENEVENT              | Buffer del comando di tipo EVENT associato per l'esecuzione in tempo reale dello script EVENT.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Il *parametro Param* contiene il testo del testo sincronizzato. Windows Media Player il testo del testo nell'area del sottotitolo codificato della **funzionalità In** riproduzione. |
| TEXT                   | Il controllo visualizza il testo associato nel div specificato da *ClosedCaption.* **captioningID**.                                                                  |
| URL                    | Il controllo apre automaticamente l'URL specificato usando il browser Internet predefinito se Impostazioni *.* **La proprietà invokeURLs** è impostata su true.                      |



 

È possibile incorporare qualsiasi altro tipo di comando, purché si fornirà codice reciproco per gestire il comando. Anche se i comandi sconosciuti vengono ignorati dal controllo Windows Media Player, vengono comunque consegnati **all'evento ScriptCommand.**

I comandi URL ricevuti dal controllo Windows Media Player vengono richiamati automaticamente nel controllo Web browser se l'Impostazioni *.* **La proprietà invokeURLs** è impostata su true. È possibile usare il *Impostazioni*. **proprietà defaultFrame** per specificare il frame di destinazione in cui viene visualizzata la pagina Web.

L'URL inviato Windows Media Player viene elaborato in relazione all'URL di base specificato dal Impostazioni *.* **proprietà baseURL.** L'URL di base viene concatenato con l'URL relativamente specificato, con un URL completamente specificato che viene passato come parametro di comando **dall'evento ScriptCommand.**

Il Windows Media Player controllo elabora sempre i comandi di tipo URL in ingresso nel modo seguente:

1.  Viene ricevuto un comando di tipo URL.
2.  *Impostazioni*. **baseURL** viene usato per creare un URL completo dall'URL relativo specificato nel comando script.
3.  *Viene chiamato ScriptCommand.*
4.  Al *termine di ScriptCommand,* *Impostazioni*. **invokeURLs è** selezionato.
5.  Se *Impostazioni*. **invokeURLs** è true e il comando è di tipo URL. Viene richiamato l'URL specificato. Se *Impostazioni*. **invokeURLs** è false oppure se il comando non è di tipo URL, il comando viene ignorato.

Quando si crea un file Windows Media, è possibile specificare il frame in cui viene visualizzato il nuovo URL concatenando due e commerciale e il nome del frame nel campo del parametro . L'esempio seguente illustra i tipici *parametri ScriptCommand.* Specifica che l'URL *mypage* deve essere avviato nel *frame myframe.*


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



L'evento ScriptCommand non viene chiamato se il file viene analizzato (inoltrato rapidamente o invertito rapidamente).

Il valore dei parametri dell'evento viene specificato da Windows Media Player ed è accessibile o passato a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, inclusa l'maiuscola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> <dt>

[**Impostazioni.baseURL**](settings-baseurl.md)
</dt> <dt>

[**Impostazioni.defaultFrame**](settings-defaultframe.md)
</dt> <dt>

[**Impostazioni.invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





