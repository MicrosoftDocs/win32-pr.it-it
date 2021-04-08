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
# <a name="using-com-objects-in-windows-script-host"></a><span data-ttu-id="b7cd0-103">Utilizzo di oggetti COM in Windows script host</span><span class="sxs-lookup"><span data-stu-id="b7cd0-103">Using COM Objects in Windows Script Host</span></span>

<span data-ttu-id="b7cd0-104">Microsoft Windows script host è un'utilità di scripting che è possibile utilizzare per eseguire script all'interno del sistema operativo di base.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-104">Microsoft Windows Script Host is a scripting utility you can use to run scripts within the base operating system.</span></span> <span data-ttu-id="b7cd0-105">È possibile utilizzare Windows script host per automatizzare le attività comuni e creare macro e script di accesso avanzati.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-105">You can use Windows Script Host to automate common tasks and to create powerful macros and logon scripts.</span></span> <span data-ttu-id="b7cd0-106">Windows script host viene incluso nei motori di scripting ActiveX VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-106">Windows Script Host comes with VBScript and JScript ActiveX scripting engines.</span></span> <span data-ttu-id="b7cd0-107">Altre società software forniscono motori di script ActiveX per linguaggi come PerlScript, PScript, Python e altri.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-107">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="b7cd0-108">Per utilizzare un oggetto COM in uno script eseguito da Windows script host, è innanzitutto necessario creare un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-108">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="b7cd0-109">Dopo la creazione di un oggetto COM, è possibile utilizzarlo negli script.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-109">After a COM object has been created, you can then use it in scripts.</span></span>

<span data-ttu-id="b7cd0-110">Windows script host è costituito da due applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-110">Windows Script Host consists of two applications.</span></span> <span data-ttu-id="b7cd0-111">Uno esegue gli script dal desktop di Windows ( `WScript.exe` ); l'altro esegue gli script dal prompt dei comandi ( `CScript.exe` ).</span><span class="sxs-lookup"><span data-stu-id="b7cd0-111">One runs scripts from the Windows desktop (`WScript.exe`); the other runs scripts from the command prompt (`CScript.exe`).</span></span>

<span data-ttu-id="b7cd0-112">Per eseguire uno script dal desktop, è sufficiente fare doppio clic su un file di script.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-112">To run a script from the desktop, simply double-click a script file.</span></span> <span data-ttu-id="b7cd0-113">I file script sono file di testo.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-113">Script files are text files.</span></span> <span data-ttu-id="b7cd0-114">Per convenzione, i file VBScript includono i `.vbs` file di estensione e JScript `.js` .</span><span class="sxs-lookup"><span data-stu-id="b7cd0-114">By convention, VBScript files have the extension `.vbs` and JScript files `.js`.</span></span>

<span data-ttu-id="b7cd0-115">Per eseguire uno script dal prompt dei comandi, eseguire l' `Cscript.exe` applicazione con una riga di comando simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="b7cd0-115">To run a script from the command prompt, run the `Cscript.exe` application with a command line such as the following:</span></span>

```console
cscript "c:\\sample scripts\\chart.vbs"
```

<span data-ttu-id="b7cd0-116">dove `c:\\sample scripts\\chart.vbs` è il percorso del file che contiene lo script.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-116">where `c:\\sample scripts\\chart.vbs` is the path to the file containing the script.</span></span>

<span data-ttu-id="b7cd0-117">È possibile stampare un elenco dei parametri supportati da Cscript.exe immettendo la riga di comando seguente:</span><span class="sxs-lookup"><span data-stu-id="b7cd0-117">You can print out a list of the parameters supported by Cscript.exe by entering the following command line:</span></span>

```console
call cscript //?
```

<span data-ttu-id="b7cd0-118">Per utilizzare un oggetto COM in uno script eseguito da Windows script host, è innanzitutto necessario creare un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-118">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="b7cd0-119">In VBScript è possibile eseguire questa operazione chiamando il `CreateObject()` metodo.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-119">In VBScript you can do this by calling the `CreateObject()` method.</span></span> <span data-ttu-id="b7cd0-120">In JScript è possibile usare l' `ActiveXObject` oggetto o il `WScript.CreateObject()` metodo.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-120">In JScript one can use either the `ActiveXObject` object or the `WScript.CreateObject()` method.</span></span> <span data-ttu-id="b7cd0-121">Nell'esempio seguente viene illustrata la chiamata `CreateObject()` tramite VBScript:</span><span class="sxs-lookup"><span data-stu-id="b7cd0-121">The following example illustrates calling `CreateObject()` using VBScript:</span></span>


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



<span data-ttu-id="b7cd0-122">Nell'esempio seguente viene illustrata la creazione di un `ActiveXObject` oggetto utilizzando JScript:</span><span class="sxs-lookup"><span data-stu-id="b7cd0-122">The following example illustrates creating an `ActiveXObject` object using JScript:</span></span>


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
<span data-ttu-id="b7cd0-123">In alternativa, usare il `WScript.CreateObject()` metodo all'interno di JScript:</span><span class="sxs-lookup"><span data-stu-id="b7cd0-123">Alternatively using `WScript.CreateObject()` method inside JScript:</span></span>

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


<span data-ttu-id="b7cd0-124">Dopo aver creato un'istanza dell'oggetto COM, è possibile scrivere uno script che usa l'oggetto, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b7cd0-124">After you have created an instance of the COM object, you can write script that uses the object, for example:</span></span>


```VB
objXL.Visible = true;
 
```



<span data-ttu-id="b7cd0-125">Oltre al metodo CreateObject e all'oggetto ActiveXObject, sia VBScript che JScript forniscono il metodo GetObject, che restituisce un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b7cd0-125">In addition to the CreateObject method and ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7cd0-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7cd0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7cd0-127">Creazione di script con oggetti COM</span><span class="sxs-lookup"><span data-stu-id="b7cd0-127">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




