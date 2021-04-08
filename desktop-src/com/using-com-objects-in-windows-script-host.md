---
title: Utilizzo di oggetti COM in Windows script host
description: Microsoft Windows script host è un'utilità di scripting che è possibile utilizzare per eseguire script all'interno del sistema operativo di base.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761585"
---
# <a name="using-com-objects-in-windows-script-host"></a>Utilizzo di oggetti COM in Windows script host

Microsoft Windows script host è un'utilità di scripting che è possibile utilizzare per eseguire script all'interno del sistema operativo di base. È possibile utilizzare Windows script host per automatizzare le attività comuni e creare macro e script di accesso avanzati. Windows script host viene incluso nei motori di scripting ActiveX VBScript e JScript. Altre società software forniscono motori di script ActiveX per linguaggi come PerlScript, PScript, Python e altri.

Per utilizzare un oggetto COM in uno script eseguito da Windows script host, è innanzitutto necessario creare un'istanza dell'oggetto. Dopo la creazione di un oggetto COM, è possibile utilizzarlo negli script.

Windows script host è costituito da due applicazioni. Uno esegue gli script dal desktop di Windows ( `WScript.exe` ); l'altro esegue gli script dal prompt dei comandi ( `CScript.exe` ).

Per eseguire uno script dal desktop, è sufficiente fare doppio clic su un file di script. I file script sono file di testo. Per convenzione, i file VBScript includono i `.vbs` file di estensione e JScript `.js` .

Per eseguire uno script dal prompt dei comandi, eseguire l' `Cscript.exe` applicazione con una riga di comando simile alla seguente:

```console
cscript "c:\\sample scripts\\chart.vbs"
```

dove `c:\\sample scripts\\chart.vbs` è il percorso del file che contiene lo script.

È possibile stampare un elenco dei parametri supportati da Cscript.exe immettendo la riga di comando seguente:

```console
call cscript //?
```

Per utilizzare un oggetto COM in uno script eseguito da Windows script host, è innanzitutto necessario creare un'istanza dell'oggetto. In VBScript è possibile eseguire questa operazione chiamando il `CreateObject()` metodo. In JScript è possibile usare l' `ActiveXObject` oggetto o il `WScript.CreateObject()` metodo. Nell'esempio seguente viene illustrata la chiamata `CreateObject()` tramite VBScript:


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



Nell'esempio seguente viene illustrata la creazione di un `ActiveXObject` oggetto utilizzando JScript:


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
In alternativa, usare il `WScript.CreateObject()` metodo all'interno di JScript:

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


Dopo aver creato un'istanza dell'oggetto COM, è possibile scrivere uno script che usa l'oggetto, ad esempio:


```VB
objXL.Visible = true;
 
```



Oltre al metodo CreateObject e all'oggetto ActiveXObject, sia VBScript che JScript forniscono il metodo GetObject, che restituisce un'istanza dell'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script con oggetti COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




