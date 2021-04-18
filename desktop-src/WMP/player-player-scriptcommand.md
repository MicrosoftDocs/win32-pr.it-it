---
title: Evento Player. ScriptCommand
description: L'evento ScriptCommand si verifica quando viene ricevuto un comando o un URL sincronizzato. | Evento Player. ScriptCommand
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Media Player di Windows Event ScriptCommand
- Windows Event ScriptCommand Media Player, classe Player
- Classe Player Windows Media Player, evento ScriptCommand
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
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333922"
---
# <a name="playerscriptcommand-event"></a>Evento Player. ScriptCommand

L'evento **ScriptCommand** si verifica quando viene ricevuto un comando o un URL sincronizzato.

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

Stringa che specifica il tipo di comando di script.

</dd> <dt>

*Param* 
</dt> <dd>

**Stringa** che specifica il comando script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

I comandi possono essere incorporati tra i suoni e le immagini di un file o di un flusso Windows Media. I comandi sono una coppia di stringhe Unicode associate a un'ora designata nel flusso. Quando il flusso raggiunge l'ora associata al comando, il controllo Windows Media Player invia un evento **ScriptCommand** con due parametri. Un parametro specifica il tipo di comando inviato e l'altro parametro specifica il comando. Il tipo di parametro viene utilizzato per determinare la modalità di elaborazione del parametro del comando. Qualsiasi tipo di comando può essere incorporato in un file o in un flusso che deve essere gestito dall'evento **ScriptCommand** .

Nella tabella seguente sono elencati i tipi di comando script elaborati automaticamente da Windows Media Player.



| Tipo                   | Descrizione                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Il controllo Visualizza il testo associato nell'elemento DIV specificato da *ClosedCaption*. **captioningID**.                                                                  |
| EVENTO                  | Indica al controllo di eseguire le istruzioni definite per l'evento specificato.                                                                                          |
| FILENAME               | Il controllo Reimposta la proprietà **URL** , tenta di aprire il file specificato e inizia immediatamente a riprodurre il nuovo flusso.                                        |
| OPENEVENT              | Memorizza nel buffer il comando del tipo di evento associato per l'esecuzione tempestiva dello script di evento.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Il parametro *param* contiene il testo lirico sincronizzato. Windows Media Player Visualizza il testo lirico nell'area didascalia chiusa della funzionalità **ora di riproduzione** . |
| TEXT                   | Il controllo Visualizza il testo associato nell'elemento DIV specificato da *ClosedCaption*. **captioningID**.                                                                  |
| URL                    | Il controllo apre automaticamente l'URL specificato utilizzando il browser Internet predefinito se le *Impostazioni*. la proprietà **invokeURLs** è impostata su true.                      |



 

È possibile incorporare qualsiasi altro tipo di comando purché si fornisca codice reciproco per gestire il comando. Sebbene i comandi sconosciuti vengano ignorati dal controllo Media Player di Windows, vengono comunque passati all'evento **ScriptCommand** .

I comandi URL ricevuti dal controllo Media Player Windows vengono richiamati automaticamente nel Web browser predefinito se le *Impostazioni*. la proprietà **invokeURLs** è impostata su true. È possibile utilizzare le *Impostazioni*. proprietà **DefaultFrame** per specificare il frame di destinazione in cui viene visualizzata la pagina Web.

L'URL inviato a Windows Media Player viene elaborato in relazione all'URL di base specificato dalle *Impostazioni*. proprietà **BaseUrl** . L'URL di base è concatenato all'URL relativamente specificato, ottenendo un URL completo che viene passato come parametro Command dall'evento **ScriptCommand** .

Il controllo Media Player Windows elabora sempre i comandi di tipo URL in arrivo nel modo seguente:

1.  Viene ricevuto un comando di tipo URL.
2.  *Impostazioni*. **BaseUrl** viene usato per creare un URL completo dall'URL relativo specificato nel comando script.
3.  Viene chiamato *ScriptCommand* .
4.  Dopo che *ScriptCommand* restituisce, *Settings*. **invokeURLs** è selezionato.
5.  Se *le impostazioni*. **invokeURLs** è true e il comando è di tipo URL, viene richiamato l'URL specificato. Se *le impostazioni*. **invokeURLs** è false o se il comando non è di tipo URL, il comando viene ignorato.

Quando si crea un file di Windows Media, è possibile specificare il frame in cui viene visualizzato il nuovo URL concatenando due e commerciali e il nome del frame nel campo del parametro. Nell'esempio seguente vengono illustrati i tipici parametri *ScriptCommand* . Specifica che è necessario avviare la *pagina* URL *nel frame frame* .


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



L'evento ScriptCommand non viene chiamato se il file viene sottoposta a scansione (veloce o invertito).

Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato. Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Settings. baseURL**](settings-baseurl.md)
</dt> <dt>

[**Settings. defaultFrame**](settings-defaultframe.md)
</dt> <dt>

[**Settings. invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





