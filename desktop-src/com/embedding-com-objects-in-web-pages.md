---
title: Incorporamento di oggetti COM nelle pagine Web
description: È possibile usare oggetti COM nelle pagine Web. A tale scopo, creare prima un'istanza di tale oggetto COM. Dopo aver creato un'istanza dell'oggetto, è possibile usarla negli script successivi in tale pagina Web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d13a92bd2de152e71ac4284ce37b977e8305f25dcb2aef5eb94d6019d115812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736892"
---
# <a name="embedding-com-objects-in-web-pages"></a>Incorporamento di oggetti COM nelle pagine Web

È possibile usare oggetti COM nelle pagine Web. A tale scopo, creare prima un'istanza di tale oggetto COM. Dopo aver creato un'istanza dell'oggetto, è possibile usarla negli script successivi in tale pagina Web.

Per creare un'istanza dell'oggetto COM in una pagina Web, è possibile usare un tag OBJECT. In alternativa, se il linguaggio di scripting fornisce un modo nativo per creare oggetti COM, è possibile creare un'istanza dell'oggetto tramite script.

Si noti che l'incorporamento di oggetti COM nelle pagine Web funziona solo con browser che supportano ActiveX e COM, ad esempio Internet Explorer.

L'esempio seguente illustra l'uso del tag OBJECT per incorporare un oggetto COM in una pagina Web:

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

È anche possibile creare un'istanza di oggetto COM nello script, se il linguaggio di scripting consente di creare oggetti COM. Ad esempio, VBScript fornisce il metodo CreateObject e JScript l'oggetto ActiveXObject. La creazione di oggetti nello script è illustrata negli esempi seguenti.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

Oltre al metodo CreateObject e all'oggetto ActiveXObject, sia VBScript che JScript il metodo GetObject, che restituisce un'istanza dell'oggetto.

Dopo aver creato un oggetto COM, è possibile fare riferimento a esso negli script successivi usando l'identificatore specificato nell'attributo ID del tag OBJECT. Nell'esempio precedente questo identificatore è stato specificato come "vid". Si noti che lo script che usa l'oggetto COM deve essere visualizzato dopo il tag OBJECT o lo script che crea l'istanza dell'oggetto. In caso contrario, l'identificatore di oggetto non è definito. Lo script seguente usa l'oggetto objXL per visualizzare le informazioni sulla versione per Microsoft Excel.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

Se si scrivono script incorporati in una pagina Web, il browser espone anche un modello a oggetti a cui gli script possono accedere. Il modello usato da Internet Explorer è conforme alla Document Object Model (DOM) proposta dal World Wide Web Consortium (W3C).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script con oggetti COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




