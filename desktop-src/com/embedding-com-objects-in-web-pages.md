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
# <a name="embedding-com-objects-in-web-pages"></a><span data-ttu-id="e30e9-105">Incorporamento di oggetti COM in pagine Web</span><span class="sxs-lookup"><span data-stu-id="e30e9-105">Embedding COM Objects in Web Pages</span></span>

<span data-ttu-id="e30e9-106">È possibile utilizzare gli oggetti COM nelle pagine Web.</span><span class="sxs-lookup"><span data-stu-id="e30e9-106">You can use COM objects in webpages.</span></span> <span data-ttu-id="e30e9-107">A tale scopo, creare innanzitutto un'istanza di tale oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="e30e9-107">To do this, first create an instance of that COM object.</span></span> <span data-ttu-id="e30e9-108">Dopo aver creato un'istanza dell'oggetto, è possibile usarla negli script successivi della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="e30e9-108">After an object instance is created, you can use it in subsequent scripts on that webpage.</span></span>

<span data-ttu-id="e30e9-109">Per creare un'istanza dell'oggetto COM in una pagina Web, è possibile usare un tag OBJECT.</span><span class="sxs-lookup"><span data-stu-id="e30e9-109">To create a COM object instance in a webpage, you can use an OBJECT tag.</span></span> <span data-ttu-id="e30e9-110">In alternativa, se il linguaggio di scripting fornisce una modalità nativa per creare oggetti COM, è possibile creare un'istanza dell'oggetto tramite script.</span><span class="sxs-lookup"><span data-stu-id="e30e9-110">Alternatively, if your scripting language provides a native way to create COM objects, you can create an object instance using script.</span></span>

<span data-ttu-id="e30e9-111">Si noti che l'incorporamento di oggetti COM nelle pagine Web funziona solo con i browser che supportano ActiveX e COM, ad esempio Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e30e9-111">Note that embedding COM objects in webpages only works with browsers that support ActiveX and COM, for example Internet Explorer.</span></span>

<span data-ttu-id="e30e9-112">Nell'esempio seguente viene illustrato l'utilizzo del tag OBJECT per incorporare un oggetto COM in una pagina Web:</span><span class="sxs-lookup"><span data-stu-id="e30e9-112">The following example illustrates using the OBJECT tag to embed a COM object in a webpage:</span></span>

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

<span data-ttu-id="e30e9-113">È inoltre possibile creare un'istanza dell'oggetto COM nello script, se il linguaggio di scripting fornisce un modo per creare oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="e30e9-113">You can also create a COM object instance in script, if your scripting language provides a way to create COM objects.</span></span> <span data-ttu-id="e30e9-114">Ad esempio, VBScript fornisce il metodo CreateObject e JScript fornisce l'oggetto ActiveXObject.</span><span class="sxs-lookup"><span data-stu-id="e30e9-114">For example, VBScript provides the CreateObject method and JScript provides the ActiveXObject object.</span></span> <span data-ttu-id="e30e9-115">Gli esempi seguenti illustrano la creazione di oggetti nello script.</span><span class="sxs-lookup"><span data-stu-id="e30e9-115">Creating objects in script is illustrated in the following examples.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

<span data-ttu-id="e30e9-116">Oltre al metodo CreateObject e all'oggetto ActiveXObject, sia VBScript che JScript forniscono il metodo GetObject, che restituisce un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e30e9-116">In addition to the CreateObject method and the ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

<span data-ttu-id="e30e9-117">Dopo la creazione di un oggetto COM, è possibile farvi riferimento negli script successivi usando l'identificatore specificato nell'attributo ID del tag OBJECT.</span><span class="sxs-lookup"><span data-stu-id="e30e9-117">After a COM object has been created, you can reference it in subsequent scripts by using the identifier specified in the OBJECT tag's ID attribute.</span></span> <span data-ttu-id="e30e9-118">Nell'esempio precedente, questo identificatore è stato specificato come "vid".</span><span class="sxs-lookup"><span data-stu-id="e30e9-118">In the preceding example, this identifier was specified as "vid."</span></span> <span data-ttu-id="e30e9-119">Si noti che lo script che usa l'oggetto COM deve essere visualizzato dopo il tag OBJECT o lo script che crea l'istanza dell'oggetto. in caso contrario, l'identificatore di oggetto non è definito.</span><span class="sxs-lookup"><span data-stu-id="e30e9-119">Note that the script that uses the COM object must appear after the OBJECT tag or script that creates the object instance; otherwise, the object identifier is undefined.</span></span> <span data-ttu-id="e30e9-120">Lo script seguente usa l'oggetto objXL per visualizzare le informazioni sulla versione di Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e30e9-120">The following script uses the objXL object to display the version information for Microsoft Excel.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

<span data-ttu-id="e30e9-121">Se si scrivono script incorporati in una pagina Web, il browser espone anche un modello a oggetti a cui gli script possono accedere.</span><span class="sxs-lookup"><span data-stu-id="e30e9-121">If you are writing scripts embedded in a webpage, the browser also exposes an object model that your scripts can access.</span></span> <span data-ttu-id="e30e9-122">Il modello utilizzato da Internet Explorer è conforme al Document Object Model (DOM) proposto dal World Wide Web Consortium (W3C).</span><span class="sxs-lookup"><span data-stu-id="e30e9-122">The model used by Internet Explorer conforms to the Document Object Model (DOM) proposed by the World Wide Web Consortium (W3C).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e30e9-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e30e9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e30e9-124">Creazione di script con oggetti COM</span><span class="sxs-lookup"><span data-stu-id="e30e9-124">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




