---
title: Esempio semplice di scripting in una pagina Web
description: Esempio semplice di scripting in una pagina Web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Controllo ActiveX di Windows Media Player, esempio di scripting
- Controllo ActiveX Windows Media Player Mobile, esempio di scripting
- Controllo ActiveX, esempio di scripting
- incorporamento, pagine Web
- Incorporamento di pagine Web, esempio di scripting
- esempio di script per l'incorporamento di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299015"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a>Esempio semplice di scripting in una pagina Web

È possibile incorporare facilmente il controllo Media Player di Windows in un file HTML usando qualsiasi linguaggio di script riconosciuto dal browser. Nell'esempio seguente viene utilizzato Microsoft JScript per creare una pagina in cui verrà riprodotto un file quando si fa clic su un pulsante e si interrompe la riproduzione del file quando si fa clic su un altro pulsante.

È possibile incorporare il controllo ActiveX di Windows Media Player in una pagina Web usando i quattro passaggi seguenti:

1.  Creare la pagina Web.
2.  Aggiungere il tag OBJECT.
3.  Aggiungere un'interfaccia utente. In questo caso, due pulsanti.
4.  Aggiungere alcune righe di codice per rispondere quando l'utente fa clic su uno dei pulsanti creati.

## <a name="creating-the-web-page"></a>Creazione della pagina Web

Il primo passaggio consiste nel creare una pagina Web HTML valida. Il codice seguente è il requisito minimo necessario per creare una pagina HTML vuota ma valida:


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a>Aggiunta del tag OBJECT

Dopo aver creato una pagina Web, è necessario aggiungere un tag OBJECT. Identifica il controllo ActiveX per il browser e configura le definizioni iniziali. È necessario inserire il tag OBJECT nel corpo del codice. Se lo si inserisce nel corpo, l'interfaccia utente predefinita di Windows Media Player sarà visibile. Se si desidera creare un'interfaccia utente personalizzata, impostare gli attributi Height e Width su 0 (zero). È anche possibile impostare il *lettore*. proprietà **uiMode** su "invisibile" quando si desidera nascondere il controllo, ma si riserva comunque spazio per l'oggetto nella pagina. Il codice seguente è consigliato quando si fornisce un'interfaccia utente personalizzata:


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



Sono necessari gli attributi di tag OBJECT seguenti:

ID

Nome che verrà usato da altre parti del codice per identificare e usare il controllo ActiveX. È possibile scegliere qualsiasi nome, purché sia un nome che non sia già usato da HTML, da estensioni HTML o dal linguaggio di scripting in uso. In questo esempio viene usato il nome "Player", ma è anche possibile denominarlo "riproduzione" o un altro elemento. È sufficiente scegliere un nome univoco per la pagina Web.

CLASSID

Numero esadecimale molto grande univoco per il controllo. Un solo controllo ha questo numero ed è il controllo ActiveX di Windows Media Player. Per evitare errori tipografici, è possibile copiare e incollare questo numero dalla documentazione. Le versioni del controllo Windows Media Player precedenti alla versione 7,0 hanno un CLASSId diverso.

## <a name="adding-a-user-interface"></a>Aggiunta di un'interfaccia utente

HTML consente un'ampia gamma di elementi dell'interfaccia utente, consentendo all'utente di interagire con la pagina Web facendo clic, premendo i tasti e altre azioni dell'utente. L'aggiunta di alcuni pulsanti di INPUT è il modo più semplice per fornire un'interfaccia utente rapida. Il codice seguente crea due pulsanti che possono rispondere all'utente. Quando si fa clic su un pulsante, viene avviata la riproduzione del flusso multimediale e l'altro pulsante lo arresta:


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



Il nome del pulsante viene usato per identificare il pulsante al codice. il valore è l'etichetta che verrà visualizzata sul pulsante e l'attributo OnClick identifica la parte del codice di scripting che verrà chiamata quando si fa clic sul pulsante.

## <a name="adding-scripting-code"></a>Aggiunta di codice di script

Il codice di scripting consente di aggiungere interattività alla pagina. Il codice di scripting può rispondere a eventi, chiamare metodi e modificare le proprietà della fase di esecuzione. Gli script estesi sono racchiusi in un set di tag di SCRIPT. Il tag SCRIPT indica al browser dove si trova il codice di script e identifica il linguaggio di scripting. Se non si identifica una lingua, la lingua predefinita sarà Microsoft JScript.

È consigliabile racchiudere lo script nei tag di commento HTML, in modo che i browser che non supportano lo script non eseguano il rendering del codice come testo. Inserire il tag SCRIPT in un punto qualsiasi all'interno del corpo del file HTML e incorporare il codice con commento racchiuso tra i tag di SCRIPT di apertura e chiusura.

Nell'esempio di codice Microsoft JScript seguente viene chiamato il controllo Media Player Windows ed eseguita un'azione appropriata in risposta al clic del pulsante corrispondente.


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



La funzione di esempio, StartMeUp, viene chiamata quando si fa clic sul pulsante contrassegnato Play e la funzione ShutMeDown viene chiamata quando si fa clic sul pulsante Interrompi.

Il codice all'interno di StartMeUp usa la proprietà URL per definire un percorso al supporto. Il supporto inizierà immediatamente a riprodursi.

Il codice ShutMeDown chiama il metodo **Stop** dell'oggetto **Controls** . Si noti che l'oggetto **Controls** viene chiamato tramite la proprietà **Controls** dell'oggetto **Player** , che ha il valore ID "Player".

L'esempio seguente illustra un esempio completo.


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



Si noti che è necessario fornire un URL valido a un nome di file valido nella proprietà URL. In questo caso il presupposto è che il file Laure. WMA si trovi nella stessa directory del file HTML.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player di Windows in una pagina Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




