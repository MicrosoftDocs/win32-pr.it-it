---
title: Incorporamento di oggetti COM in pagine Web
description: È possibile utilizzare gli oggetti COM nelle pagine Web. A tale scopo, creare innanzitutto un'istanza di tale oggetto COM. Dopo aver creato un'istanza dell'oggetto, è possibile usarla negli script successivi della pagina Web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329375"
---
# <a name="embedding-com-objects-in-web-pages"></a>Incorporamento di oggetti COM in pagine Web

È possibile utilizzare gli oggetti COM nelle pagine Web. A tale scopo, creare innanzitutto un'istanza di tale oggetto COM. Dopo aver creato un'istanza dell'oggetto, è possibile usarla negli script successivi della pagina Web.

Per creare un'istanza dell'oggetto COM in una pagina Web, è possibile usare un tag OBJECT. In alternativa, se il linguaggio di scripting fornisce una modalità nativa per creare oggetti COM, è possibile creare un'istanza dell'oggetto tramite script.

Si noti che l'incorporamento di oggetti COM nelle pagine Web funziona solo con i browser che supportano ActiveX e COM, ad esempio Internet Explorer.

Nell'esempio seguente viene illustrato l'utilizzo del tag OBJECT per incorporare un oggetto COM in una pagina Web:

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

È inoltre possibile creare un'istanza dell'oggetto COM nello script, se il linguaggio di scripting fornisce un modo per creare oggetti COM. Ad esempio, VBScript fornisce il metodo CreateObject e JScript fornisce l'oggetto ActiveXObject. Gli esempi seguenti illustrano la creazione di oggetti nello script.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

Oltre al metodo CreateObject e all'oggetto ActiveXObject, sia VBScript che JScript forniscono il metodo GetObject, che restituisce un'istanza dell'oggetto.

Dopo la creazione di un oggetto COM, è possibile farvi riferimento negli script successivi usando l'identificatore specificato nell'attributo ID del tag OBJECT. Nell'esempio precedente, questo identificatore è stato specificato come "vid". Si noti che lo script che usa l'oggetto COM deve essere visualizzato dopo il tag OBJECT o lo script che crea l'istanza dell'oggetto. in caso contrario, l'identificatore di oggetto non è definito. Lo script seguente usa l'oggetto objXL per visualizzare le informazioni sulla versione di Microsoft Excel.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

Se si scrivono script incorporati in una pagina Web, il browser espone anche un modello a oggetti a cui gli script possono accedere. Il modello utilizzato da Internet Explorer è conforme al Document Object Model (DOM) proposto dal World Wide Web Consortium (W3C).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script con oggetti COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




