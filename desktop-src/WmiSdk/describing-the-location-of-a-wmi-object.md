---
description: Concettualmente simile a un Uniform Resource Locator (URL), il percorso di un oggetto WMI è una stringa che identifica in modo univoco lo spazio dei nomi in un server, una classe all'interno di uno spazio dei nomi o istanze di una classe.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Descrizione della posizione di un oggetto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310375"
---
# <a name="describing-the-location-of-a-wmi-object"></a><span data-ttu-id="8cb18-103">Descrizione della posizione di un oggetto WMI</span><span class="sxs-lookup"><span data-stu-id="8cb18-103">Describing the Location of a WMI Object</span></span>

<span data-ttu-id="8cb18-104">Concettualmente simile a un Uniform Resource Locator (URL), il percorso di un oggetto WMI è una stringa che identifica in modo univoco lo spazio dei nomi in un server, una classe all'interno di uno spazio dei nomi o istanze di una classe.</span><span class="sxs-lookup"><span data-stu-id="8cb18-104">Conceptually similar to a Uniform Resource Locator (URL), a WMI object path is a string that uniquely identifies the namespace on a server, a class within a namespace, or instances of a class.</span></span> <span data-ttu-id="8cb18-105">Il percorso di un oggetto è gerarchico e contiene diversi elementi che descrivono la posizione dell'oggetto in questione.</span><span class="sxs-lookup"><span data-stu-id="8cb18-105">An object path is hierarchical, and contains several elements that describe the location of the object in question.</span></span> <span data-ttu-id="8cb18-106">Come i percorsi di file, i percorsi degli oggetti WMI possono essere descritti in modo completo o specificato come percorso relativo.</span><span class="sxs-lookup"><span data-stu-id="8cb18-106">Like file paths, WMI object paths can be described in full or specified as a relative path.</span></span>

<span data-ttu-id="8cb18-107">Lo spazio dei nomi di un oggetto WMI è elencato nella pagina di riferimento di WMI.</span><span class="sxs-lookup"><span data-stu-id="8cb18-107">The namespace of a WMI object is listed on the WMI reference page.</span></span> <span data-ttu-id="8cb18-108">Ad esempio, il percorso della maggior parte delle classi supportate dai [provider WMI cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) si trova nello \\ \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="8cb18-108">For example, the location of most of the classes supported by the [CIMWin32 WMI Providers](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) are located in the \\root\\cimv2 namespace.</span></span> <span data-ttu-id="8cb18-109">Il codice di PowerShell seguente descrive una chiamata per recuperare l'oggetto [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) nel computer locale:</span><span class="sxs-lookup"><span data-stu-id="8cb18-109">The following PowerShell code describes a call to retrieve the [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) object on your local machine:</span></span>

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

<span data-ttu-id="8cb18-110">In alternativa, un'istanza specifica di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) può avere il percorso seguente dalla proprietà [**SWbemObject. Path \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb18-110">Alternately, a specific instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) may have the following path from the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

<span data-ttu-id="8cb18-111">Nell'esempio seguente viene illustrato il percorso relativo di questa istanza, come visualizzato visualizzando la proprietà [**RelPath**](swbemobjectpath-relpath.md) dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) restituito dalla chiamata a [**SWbemObject. Path \_**](swbemobject-path-.md).</span><span class="sxs-lookup"><span data-stu-id="8cb18-111">The following example shows the relative path to this instance, as seen by displaying the [**Relpath**](swbemobjectpath-relpath.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the call to [**SWbemObject.Path\_**](swbemobject-path-.md).</span></span>

`Win32_LogicalDisk.DeviceID="A:"`

<span data-ttu-id="8cb18-112">Si noti che **DeviceID** è la proprietà chiave della [**classe \_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="8cb18-112">Note that **DeviceID** is the key property of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

## <a name="c"></a><span data-ttu-id="8cb18-113">C++</span><span class="sxs-lookup"><span data-stu-id="8cb18-113">C++</span></span>

<span data-ttu-id="8cb18-114">Nella tabella seguente sono elencati i tipi di percorso degli oggetti e i metodi associati che richiedono percorsi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="8cb18-114">The following table lists object path types and the associated methods that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8cb18-115">Tipo di percorso dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="8cb18-115">Object path type</span></span></th>
<th><span data-ttu-id="8cb18-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="8cb18-116">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cb18-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span><span class="sxs-lookup"><span data-stu-id="8cb18-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span></span></td>
<td><dl><span data-ttu-id="8cb18-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices::OpenNamespace</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cb18-119"><a href="describing-a-class-object-path.md">Classe</a></span><span class="sxs-lookup"><span data-stu-id="8cb18-119"><a href="describing-a-class-object-path.md">Class</a></span></span></td>
<td><dl><span data-ttu-id="8cb18-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices::ExecMethod</strong></a></span></span><br />
<span data-ttu-id="8cb18-121">[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span><span class="sxs-lookup"><span data-stu-id="8cb18-121">[<strong>IWbemServices::ExecMethodAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cb18-122"><a href="describing-a-class-object-path.md">Classe</a> o <a href="describing-an-instance-object-path.md">istanza</a></span><span class="sxs-lookup"><span data-stu-id="8cb18-122"><a href="describing-a-class-object-path.md">Class</a> or <a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="8cb18-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices::GetObject</strong></a></span></span><br />
<span data-ttu-id="8cb18-124">[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span><span class="sxs-lookup"><span data-stu-id="8cb18-124">[<strong>IWbemServices::GetObjectAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cb18-125"><a href="describing-an-instance-object-path.md">Istanza</a></span><span class="sxs-lookup"><span data-stu-id="8cb18-125"><a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="8cb18-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::DeleteInstance</strong></a></span></span><br />
<span data-ttu-id="8cb18-127">[<strong>IWbemServices::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span><span class="sxs-lookup"><span data-stu-id="8cb18-127">[<strong>IWbemServices::DeleteInstanceAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a><span data-ttu-id="8cb18-128">Script</span><span class="sxs-lookup"><span data-stu-id="8cb18-128">Script</span></span>

<span data-ttu-id="8cb18-129">I percorsi degli oggetti possono essere costruiti in diversi modi:</span><span class="sxs-lookup"><span data-stu-id="8cb18-129">Object paths can be constructed in several ways:</span></span>

-   <span data-ttu-id="8cb18-130">Recuperare la proprietà di un metodo che restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb18-130">Retrieve the property of a method that returns an [**SWbemObjectPath**](swbemobjectpath.md) object.</span></span>
-   <span data-ttu-id="8cb18-131">Recuperare la proprietà [**SWbemObject. \_ path**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb18-131">Retrieve the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>
-   <span data-ttu-id="8cb18-132">Creare una variabile di stringa che contiene il percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cb18-132">Create a string variable that contains the object path.</span></span>

<span data-ttu-id="8cb18-133">Nella tabella seguente sono elencati gli oggetti di scripting che richiedono percorsi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="8cb18-133">The following table lists the scripting objects that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8cb18-134">Oggetto di scripting</span><span class="sxs-lookup"><span data-stu-id="8cb18-134">Scripting object</span></span></th>
<th><span data-ttu-id="8cb18-135">Metodo</span><span class="sxs-lookup"><span data-stu-id="8cb18-135">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cb18-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span></span></td>
<td><dl><span data-ttu-id="8cb18-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span></span><br />
<span data-ttu-id="8cb18-138">[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-138">[<strong>AssociatorsOfAsync</strong>](swbemservices-associatorsofasync.md)</span></span><br />
<span data-ttu-id="8cb18-139">[<strong>Elimina</strong>] (swbemservices-delete.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-139">[<strong>Delete</strong>](swbemservices-delete.md)</span></span><br />
<span data-ttu-id="8cb18-140">[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-140">[<strong>DeleteAsync</strong>](swbemservices-deleteasync.md)</span></span><br />
<span data-ttu-id="8cb18-141">[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-141">[<strong>ExecMethod</strong>](swbemservices-execmethod.md)</span></span><br />
<span data-ttu-id="8cb18-142">[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-142">[<strong>ExecMethodAsync</strong>](swbemservices-execmethodasync.md)</span></span><br />
<span data-ttu-id="8cb18-143">[<strong>Get</strong>] (swbemservices-get.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-143">[<strong>Get</strong>](swbemservices-get.md)</span></span><br />
<span data-ttu-id="8cb18-144">[<strong>GetAsync</strong>] (swbemservices-getasync.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-144">[<strong>GetAsync</strong>](swbemservices-getasync.md)</span></span><br />
<span data-ttu-id="8cb18-145">[<strong>ReferencesTo</strong>] (swbemservices-referencesto.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-145">[<strong>ReferencesTo</strong>](swbemservices-referencesto.md)</span></span><br />
<span data-ttu-id="8cb18-146">[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)</span><span class="sxs-lookup"><span data-stu-id="8cb18-146">[<strong>ReferencesToAsync</strong>](swbemservices-referencestoasync.md)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cb18-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span></span></td>
<td><dl><span data-ttu-id="8cb18-148"><a href="swbemobjectset-item.md"><strong>Elemento</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cb18-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
