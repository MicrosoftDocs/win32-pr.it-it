---
description: 'Altre informazioni su: membri di istanza'
title: 'Membri di istanza '
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8ba8dad079feba566dbb8fca873fcea19af778ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879845"
---
# <a name="instance-members"></a><span data-ttu-id="cbab8-103">Membri di istanza </span><span class="sxs-lookup"><span data-stu-id="cbab8-103">Instance members</span></span>

<span data-ttu-id="cbab8-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="cbab8-104">Include protected members</span></span>  
<span data-ttu-id="cbab8-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="cbab8-105">Include inherited members</span></span>  

<span data-ttu-id="cbab8-106">Classe che incapsula un [JET_INSTANCE](./jet-instance-structure.md) in un oggetto eliminabile.</span><span class="sxs-lookup"><span data-stu-id="cbab8-106">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="cbab8-107">L'istanza deve essere chiusa per ultima e la chiusura dell'istanza rilascia tutte le altre risorse per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-107">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

<span data-ttu-id="cbab8-108">Il tipo di [istanza](./instance-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="cbab8-108">The [Instance](./instance-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="cbab8-109">Costruttori</span><span class="sxs-lookup"><span data-stu-id="cbab8-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cbab8-110">Nome</span><span class="sxs-lookup"><span data-stu-id="cbab8-110">Name</span></span></th>
<th><span data-ttu-id="cbab8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbab8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-113"><a href="dn350924(v=exchg.10).md">Istanza (stringa)</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-113"><a href="dn350924(v=exchg.10).md">Instance(String)</a></span></span></td>
<td><span data-ttu-id="cbab8-114">Inizializza una nuova istanza della classe dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-114">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="cbab8-115">Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="cbab8-115">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-117"><a href="dn350927(v=exchg.10).md">Instance (String, String)</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-117"><a href="dn350927(v=exchg.10).md">Instance(String, String)</a></span></span></td>
<td><span data-ttu-id="cbab8-118">Inizializza una nuova istanza della classe dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-118">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="cbab8-119">Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="cbab8-119">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-121"><a href="dn350948(v=exchg.10).md">Instance (String, String, TermGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-121"><a href="dn350948(v=exchg.10).md">Instance(String, String, TermGrbit)</a></span></span></td>
<td><span data-ttu-id="cbab8-122">Inizializza una nuova istanza della classe dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-122">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="cbab8-123">Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="cbab8-123">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbab8-124">Inizio</span><span class="sxs-lookup"><span data-stu-id="cbab8-124">Top</span></span>

## <a name="properties"></a><span data-ttu-id="cbab8-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbab8-125">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cbab8-126">Nome</span><span class="sxs-lookup"><span data-stu-id="cbab8-126">Name</span></span></th>
<th><span data-ttu-id="cbab8-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbab8-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="cbab8-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span></span></td>
<td><span data-ttu-id="cbab8-130">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-130">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="cbab8-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span></span></td>
<td><span data-ttu-id="cbab8-133">Ereditato da <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-133">(Inherited from <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="cbab8-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span></span></td>
<td><span data-ttu-id="cbab8-136">Ottiene il JET_INSTANCE contenuto in questa istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-136">Gets the JET_INSTANCE that this instance contains.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="cbab8-138"><a href="dn350962(v=exchg.10).md">Parametri</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-138"><a href="dn350962(v=exchg.10).md">Parameters</a></span></span></td>
<td><span data-ttu-id="cbab8-139">Ottiene l'oggetto InstanceParameters per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-139">Gets the InstanceParameters for this instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="cbab8-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span></span></td>
<td><span data-ttu-id="cbab8-142">Ottiene o imposta TermGrbit per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-142">Gets or sets the TermGrbit for this instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbab8-143">Inizio</span><span class="sxs-lookup"><span data-stu-id="cbab8-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="cbab8-144">Metodi</span><span class="sxs-lookup"><span data-stu-id="cbab8-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cbab8-145">Nome</span><span class="sxs-lookup"><span data-stu-id="cbab8-145">Name</span></span></th>
<th><span data-ttu-id="cbab8-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbab8-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Close</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Close</a></span></span></td>
<td><span data-ttu-id="cbab8-149">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-149">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span></span></td>
<td><span data-ttu-id="cbab8-152">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-152">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span></span></td>
<td><span data-ttu-id="cbab8-155">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-155">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span></span></td>
<td><span data-ttu-id="cbab8-158">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-158">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="cbab8-161">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-161">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="cbab8-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose (valore booleano)</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="cbab8-164">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-164">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="cbab8-167">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="cbab8-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="cbab8-170">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-170">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="cbab8-173">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="cbab8-176">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-176">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-178"><a href="dn350932(v=exchg.10).md">Init ()</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-178"><a href="dn350932(v=exchg.10).md">Init()</a></span></span></td>
<td><span data-ttu-id="cbab8-179">Inizializzare il JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="cbab8-179">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-181"><a href="dn350954(v=exchg.10).md">Init (InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-181"><a href="dn350954(v=exchg.10).md">Init(InitGrbit)</a></span></span></td>
<td><span data-ttu-id="cbab8-182">Inizializzare il JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="cbab8-182">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-184"><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-184"><a href="dn350934(v=exchg.10).md">Init(JET_RSTINFO, InitGrbit)</a></span></span></td>
<td><span data-ttu-id="cbab8-185">Inizializzare il JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="cbab8-185">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="cbab8-186">Questa API richiede almeno la versione vista di ESENT.</span><span class="sxs-lookup"><span data-stu-id="cbab8-186">This API requires at least the Vista version of ESENT.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="cbab8-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="cbab8-189">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-189">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="cbab8-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span></span></td>
<td><span data-ttu-id="cbab8-192">Rilasciare l'handle per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="cbab8-192">Release the handle for this instance.</span></span> <span data-ttu-id="cbab8-193">Esegue l'override di <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-193">(Overrides <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle.ReleaseHandle()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="cbab8-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span></span></td>
<td><span data-ttu-id="cbab8-196">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-196">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span></span></td>
<td><span data-ttu-id="cbab8-199">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-199">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-201"><a href="dn350935(v=exchg.10).md">Termine</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-201"><a href="dn350935(v=exchg.10).md">Term</a></span></span></td>
<td><span data-ttu-id="cbab8-202">Terminare il JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="cbab8-202">Terminate the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="cbab8-204"><a href="dn350960(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-204"><a href="dn350960(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="cbab8-205">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta l' <a href="dn350923(v=exchg.10).md">istanza</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="cbab8-205">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn350923(v=exchg.10).md">Instance</a>.</span></span> <span data-ttu-id="cbab8-206">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-206">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbab8-207">Inizio</span><span class="sxs-lookup"><span data-stu-id="cbab8-207">Top</span></span>

## <a name="operators"></a><span data-ttu-id="cbab8-208">Operatori</span><span class="sxs-lookup"><span data-stu-id="cbab8-208">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cbab8-209">Nome</span><span class="sxs-lookup"><span data-stu-id="cbab8-209">Name</span></span></th>
<th><span data-ttu-id="cbab8-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbab8-210">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="cbab8-213"><a href="dn350950(v=exchg.10).md">Implicita (da istanza a JET_INSTANCE)</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-213"><a href="dn350950(v=exchg.10).md">Implicit(Instance to JET_INSTANCE)</a></span></span></td>
<td><span data-ttu-id="cbab8-214">Fornire la conversione implicita di un oggetto istanza a una struttura JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="cbab8-214">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="cbab8-215">Questa operazione viene eseguita in modo che un'istanza possa essere utilizzata ovunque sia necessario un JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="cbab8-215">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbab8-216">Inizio</span><span class="sxs-lookup"><span data-stu-id="cbab8-216">Top</span></span>

## <a name="fields"></a><span data-ttu-id="cbab8-217">Campi</span><span class="sxs-lookup"><span data-stu-id="cbab8-217">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="cbab8-218">Nome</span><span class="sxs-lookup"><span data-stu-id="cbab8-218">Name</span></span></th>
<th><span data-ttu-id="cbab8-219">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbab8-219">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Campo protetto" alt="Protected field" /></td>
<td><span data-ttu-id="cbab8-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">gestire</a></span><span class="sxs-lookup"><span data-stu-id="cbab8-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">handle</a></span></span></td>
<td><span data-ttu-id="cbab8-222">Ereditato da <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="cbab8-222">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbab8-223">Inizio</span><span class="sxs-lookup"><span data-stu-id="cbab8-223">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="cbab8-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbab8-224">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cbab8-225">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cbab8-225">Reference</span></span>

[<span data-ttu-id="cbab8-226">Classe dell'istanza</span><span class="sxs-lookup"><span data-stu-id="cbab8-226">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="cbab8-227">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cbab8-227">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
