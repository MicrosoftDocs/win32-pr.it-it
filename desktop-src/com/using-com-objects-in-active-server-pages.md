---
title: Utilizzo di oggetti COM in pagine Active Server
description: È possibile creare script per oggetti COM in applicazioni di Active Server Pages (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328636"
---
# <a name="using-com-objects-in-active-server-pages"></a><span data-ttu-id="8ca5e-103">Utilizzo di oggetti COM in pagine Active Server</span><span class="sxs-lookup"><span data-stu-id="8ca5e-103">Using COM Objects in Active Server Pages</span></span>

<span data-ttu-id="8ca5e-104">È possibile creare script per oggetti COM in applicazioni di Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="8ca5e-104">You can script COM objects in Active Server Pages (ASP) applications.</span></span> <span data-ttu-id="8ca5e-105">A tale scopo, è innanzitutto necessario creare un'istanza dell'oggetto utilizzando il tag OBJECT oppure chiamando il metodo CreateObject dell'oggetto ASP server.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-105">To do so, you must first create an instance of the object either by using the OBJECT tag or by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="8ca5e-106">Una volta creato un oggetto COM, è possibile utilizzarlo negli script successivi della pagina ASP.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-106">Once a COM object has been created, you can use it in subsequent scripts on the ASP page.</span></span>

<span data-ttu-id="8ca5e-107">Con ASP è possibile utilizzare molti tipi diversi di motori di scripting, ciascuno dei quali supporta un linguaggio di scripting diverso.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-107">Using ASP, you can work with many different types of scripting engines, each of which supports a different scripting language.</span></span> <span data-ttu-id="8ca5e-108">ASP viene fornita con i motori di script VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-108">ASP comes with VBScript and JScript scripting engines.</span></span> <span data-ttu-id="8ca5e-109">È anche possibile collegare motori di scripting sviluppati da altre società per supportare linguaggi quali PerlScript, PScript, Python e altri.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-109">You can also plug in scripting engines developed by other companies to support languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="8ca5e-110">Se non si imposta il linguaggio di scripting per una pagina ASP, VBScript è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-110">If you do not set the scripting language for an ASP page, VBScript is the default.</span></span> <span data-ttu-id="8ca5e-111">Per specificare un linguaggio di script diverso da VBScript, includere una riga come la seguente nella parte superiore di ogni pagina ASP:</span><span class="sxs-lookup"><span data-stu-id="8ca5e-111">To specify a scripting language other than VBScript, include a line such as the following at the top of each ASP page:</span></span>

``` syntax
<%@ LANGUAGE=JScript %>
 
```

<span data-ttu-id="8ca5e-112">Per utilizzare un oggetto COM in una pagina ASP, è innanzitutto necessario creare un'istanza di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-112">To use a COM object in an ASP page, you must first create an instance of that object.</span></span> <span data-ttu-id="8ca5e-113">A tale scopo, usare il tag OBJECT e specificare il valore "SERVER" per l'attributo RUNAt, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-113">You do this by using the OBJECT tag and specifying the value "SERVER" for the RUNAT attribute, as shown in the following example.</span></span> <span data-ttu-id="8ca5e-114">Per impostazione predefinita, il tag OBJECT crea un'istanza dell'oggetto nel client.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-114">By default, the OBJECT tag creates an instance of the object on the client.</span></span> <span data-ttu-id="8ca5e-115">L'impostazione dell'attributo RUNAt sul SERVER comporta la creazione dell'oggetto nel server.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-115">Setting the RUNAT attribute to SERVER causes the object to be created on the server.</span></span> <span data-ttu-id="8ca5e-116">L'oggetto deve essere eseguito nel server per poter essere utilizzato da ASP.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-116">The object must run on the server in order to be used by ASP.</span></span>

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

<span data-ttu-id="8ca5e-117">È inoltre possibile creare un'istanza di un oggetto COM in una pagina ASP chiamando il metodo CreateObject dell'oggetto server ASP.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-117">You can also create an instance of a COM object on an ASP page by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="8ca5e-118">L'utilizzo di server. CreateObject è più lento della creazione dell'oggetto utilizzando un tag OBJECT, ma è leggermente più leggibile perché specifica l'identificatore a livello di codice anziché l'identificatore di classe dell'oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-118">Using Server.CreateObject is slower than creating the object using an OBJECT tag, but it is slightly more readable because it specifies the programmatic identifier instead of the class identifier of the COM object.</span></span> <span data-ttu-id="8ca5e-119">L'oggetto server è esposto da ASP e non è necessario crearlo.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-119">The Server object is exposed by ASP and does not need to be created.</span></span> <span data-ttu-id="8ca5e-120">Negli esempi seguenti viene illustrato come chiamare il metodo Server. CreateObject.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-120">How to call Server.CreateObject is illustrated in the following examples.</span></span> <span data-ttu-id="8ca5e-121">Il primo esempio è VBScript:</span><span class="sxs-lookup"><span data-stu-id="8ca5e-121">The first example is VBScript:</span></span>

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="8ca5e-122">L'esempio successivo è JScript:</span><span class="sxs-lookup"><span data-stu-id="8ca5e-122">The next example is JScript:</span></span>

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="8ca5e-123">La chiamata a CreateObject è più lenta rispetto all'uso del tag OBJECT per creare un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-123">Calling CreateObject is slower than using the OBJECT tag to create a COM object.</span></span> <span data-ttu-id="8ca5e-124">Nelle applicazioni in cui le prestazioni sono critiche è necessario usare il tag OBJECT.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-124">In applications where performance is critical, you should use the OBJECT tag.</span></span>

<span data-ttu-id="8ca5e-125">Una volta creata un'istanza dell'oggetto COM, è possibile utilizzarla negli script.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-125">After you have created an instance of the COM object, you can use it in scripts.</span></span> <span data-ttu-id="8ca5e-126">Questa operazione è illustrata nell'esempio VBScript seguente, che imposta il valore della proprietà Border dell'oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="8ca5e-126">Doing this is illustrated in the VBScript example following, which sets the value of the COM object's Border property.</span></span>

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a><span data-ttu-id="8ca5e-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ca5e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ca5e-128">Creazione di script con oggetti COM</span><span class="sxs-lookup"><span data-stu-id="8ca5e-128">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




