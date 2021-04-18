---
description: Fornisce funzionalità di accesso semisincrono e un esempio di codice per eseguire una chiamata al metodo semisincrono.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Esecuzione di una chiamata semisincrono con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315197"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a><span data-ttu-id="6627d-103">Esecuzione di una chiamata semisincrono con VBScript</span><span class="sxs-lookup"><span data-stu-id="6627d-103">Making a Semisynchronous Call with VBScript</span></span>

<span data-ttu-id="6627d-104">Alcuni metodi WMI possono restituire raccolte di grandi dimensioni, causando l'interruzione della risposta degli script.</span><span class="sxs-lookup"><span data-stu-id="6627d-104">Some WMI methods can return large collections, causing scripts to stop responding.</span></span> <span data-ttu-id="6627d-105">Nello script, l'accesso semisincrono è l'impostazione predefinita e Strumentazione gestione Windows (WMI) imposta **wbemFlagReturnImmediately** per le chiamate che possono restituire raccolte di oggetti di grandi dimensioni, ad esempio i seguenti metodi [**SWbemServices**](swbemservices.md) : [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)e [**ReferencesTo**](swbemservices-referencesto.md).</span><span class="sxs-lookup"><span data-stu-id="6627d-105">In script, semisynchronous access is the default, and Windows Management Instrumentation (WMI) sets **wbemFlagReturnImmediately** for calls that can return large object collections such as the following [**SWbemServices**](swbemservices.md) methods: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md), and [**ReferencesTo**](swbemservices-referencesto.md).</span></span>

<span data-ttu-id="6627d-106">L'accesso semisincrono che **USA wbemFlagReturnImmediately** impostato nel parametro *iFlags* è anche il valore predefinito per le chiamate che possono restituire set di oggetti di grandi dimensioni per i metodi [**SWbemObject**](swbemobject.md) seguenti: [**istanze \_**](swbemobject-instances-.md), [**sottoclassi \_**](swbemobject-subclasses-.md), [**associatori \_**](swbemobject-associators-.md)e [**riferimenti \_**](swbemobject-references-.md).</span><span class="sxs-lookup"><span data-stu-id="6627d-106">Semisynchronous access that uses **wbemFlagReturnImmediately** set in the *IFlags* parameter is also the default for calls that can return large object sets for the following [**SWbemObject**](swbemobject.md) methods: [**Instances\_**](swbemobject-instances-.md), [**Subclasses\_**](swbemobject-subclasses-.md), [**Associators\_**](swbemobject-associators-.md), and [**References\_**](swbemobject-references-.md).</span></span>

<span data-ttu-id="6627d-107">Per ridurre l'utilizzo delle risorse di memoria WMI durante l'elaborazione di una raccolta di oggetti di grandi dimensioni, includere il valore di **wbemFlagForwardOnly** nel parametro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="6627d-107">To reduce the WMI memory resource usage when processing a large collection of objects, include the value of **wbemFlagForwardOnly** in the *IFlags* parameter.</span></span> <span data-ttu-id="6627d-108">L'utilizzo di **wbemFlagForwardOnly** fa sì che WMI crei un enumeratore di sola trasmissione che non consente la rimozione della raccolta e l'accesso di nuovo agli elementi.</span><span class="sxs-lookup"><span data-stu-id="6627d-108">Using **wbemFlagForwardOnly** causes WMI to create a forward-only enumerator that does not allow rewinding the collection and accessing items again.</span></span>

<span data-ttu-id="6627d-109">WMI Elimina la memoria per ogni oggetto perché l'istruzione **for each** elabora un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6627d-109">WMI eliminates the memory for each object as the **For Each** statement processes an object.</span></span> <span data-ttu-id="6627d-110">Non è possibile chiamare il metodo **count** per una raccolta quando il flag **wbemFlagForwardOnly** è stato impostato sulla chiamata che ha ottenuto la raccolta.</span><span class="sxs-lookup"><span data-stu-id="6627d-110">You cannot call the **Count** method for a collection when the **wbemFlagForwardOnly** flag was set on the call that obtained the collection.</span></span> <span data-ttu-id="6627d-111">Si noti che il parametro *iFlags* ha **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** impostati per impostazione predefinita per il metodo [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="6627d-111">Note that the *IFlags* parameter has **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** set by default for the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method.</span></span>

<span data-ttu-id="6627d-112">Nella procedura seguente viene descritto come utilizzare VBScript per effettuare una chiamata semisincrono.</span><span class="sxs-lookup"><span data-stu-id="6627d-112">The following procedure describes how to use VBScript to make a semisynchronous call.</span></span>

<span data-ttu-id="6627d-113">**Per eseguire una chiamata semisincrono in VBScript**</span><span class="sxs-lookup"><span data-stu-id="6627d-113">**To make a semisynchronous call in VBScript**</span></span>

1.  <span data-ttu-id="6627d-114">Impostare il parametro *iFlags* sul valore di [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="6627d-114">Set the *IFlags* parameter to the value of [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>
2.  <span data-ttu-id="6627d-115">Eseguire la normale chiamata sincrona per [**SWbemServices.ExecQuery**](swbemservices-execquery.md) o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) con il valore *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="6627d-115">Make the normal synchronous call for [**SWbemServices.ExecQuery**](swbemservices-execquery.md) or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) with the *iFlags* value.</span></span>
3.  <span data-ttu-id="6627d-116">Se si desidera considerare gli oggetti restituiti dalla chiamata come raccolta, utilizzare una sintassi di enumerazione come VBScript **per ognuno** di essi.</span><span class="sxs-lookup"><span data-stu-id="6627d-116">If you want to treat the objects returned by the call as a collection, use an enumeration syntax such as VBScript **For Each**.</span></span> <span data-ttu-id="6627d-117">Poiché ogni oggetto viene restituito, viene elaborato come elemento successivo nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6627d-117">As each object is returned, it is processed as the next item in the collection.</span></span>
4.  <span data-ttu-id="6627d-118">Creare un enumeratore di sola trasmissione combinando il valore di **wbemFlagReturnImmediately** con il valore di **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="6627d-118">Create a forward-only enumerator by combining the value of **wbemFlagReturnImmediately** with the value of **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="6627d-119">Il valore decimale di questa operazione o è 48.</span><span class="sxs-lookup"><span data-stu-id="6627d-119">The decimal value of this OR operation is 48.</span></span> <span data-ttu-id="6627d-120">Queste costanti sono definite nella libreria dei tipi wbemdisp. tlb per Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6627d-120">These constants are defined in the wbemdisp.tlb type library for Visual Basic.</span></span> <span data-ttu-id="6627d-121">La maggior parte dei linguaggi di scripting usa il valore numerico o definisce una costante.</span><span class="sxs-lookup"><span data-stu-id="6627d-121">Most scripting languages use the numeric value or define a constant.</span></span> <span data-ttu-id="6627d-122">Per ulteriori informazioni, vedere [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="6627d-122">For more information, see [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>

<span data-ttu-id="6627d-123">Nell'esempio di codice seguente viene illustrato come eseguire una chiamata al metodo semisincrono.</span><span class="sxs-lookup"><span data-stu-id="6627d-123">The following code example shows how to make a semisynchronous method call.</span></span> <span data-ttu-id="6627d-124">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6627d-124">For more information, see [Calling a Method](calling-a-method.md).</span></span>


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a><span data-ttu-id="6627d-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6627d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6627d-126">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="6627d-126">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 



