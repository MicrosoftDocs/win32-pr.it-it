---
description: 'Altre informazioni su: membri di ColumnStream'
title: 'Membri di ColumnStream '
TOCTitle: ColumnStream members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream_members(v=EXCHG.10)
ms:contentKeyID: 55101147
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9f35c0e000329bc98e2f9fd5873cd724516271d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552189"
---
# <a name="columnstream-members"></a><span data-ttu-id="96ee0-103">Membri di ColumnStream </span><span class="sxs-lookup"><span data-stu-id="96ee0-103">ColumnStream members</span></span>

<span data-ttu-id="96ee0-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="96ee0-104">Include protected members</span></span>  
<span data-ttu-id="96ee0-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="96ee0-105">Include inherited members</span></span>  

<span data-ttu-id="96ee0-106">Questa classe fornisce un'interfaccia di flusso a una colonna con valore Long, ovvero una colonna di tipo [LongBinary](./jet-coltyp-enumeration.md) o [LONGTEXT](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="96ee0-106">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="96ee0-107">Il tipo [ColumnStream](./columnstream-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="96ee0-107">The [ColumnStream](./columnstream-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="96ee0-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="96ee0-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="96ee0-109">Nome</span><span class="sxs-lookup"><span data-stu-id="96ee0-109">Name</span></span></th>
<th><span data-ttu-id="96ee0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96ee0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span></span></td>
<td><span data-ttu-id="96ee0-113">Inizializza una nuova istanza della classe ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="96ee0-113">Initializes a new instance of the ColumnStream class.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96ee0-114">Inizio</span><span class="sxs-lookup"><span data-stu-id="96ee0-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="96ee0-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96ee0-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="96ee0-116">Nome</span><span class="sxs-lookup"><span data-stu-id="96ee0-116">Name</span></span></th>
<th><span data-ttu-id="96ee0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96ee0-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span></span></td>
<td><span data-ttu-id="96ee0-120">Ottiene un valore che indica se il flusso supporta la lettura.</span><span class="sxs-lookup"><span data-stu-id="96ee0-120">Gets a value indicating whether the stream supports reading.</span></span> <span data-ttu-id="96ee0-121">Esegue l'override di <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream. CanRead</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-121">(Overrides <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream.CanRead</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span></span></td>
<td><span data-ttu-id="96ee0-124">Ottiene un valore che indica se il flusso supporta la ricerca.</span><span class="sxs-lookup"><span data-stu-id="96ee0-124">Gets a value indicating whether the stream supports seeking.</span></span> <span data-ttu-id="96ee0-125">Esegue l'override di <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream. CanSeek</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-125">(Overrides <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream.CanSeek</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span></span></td>
<td><span data-ttu-id="96ee0-128">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-128">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span></span></td>
<td><span data-ttu-id="96ee0-131">Ottiene un valore che indica se il flusso supporta la scrittura.</span><span class="sxs-lookup"><span data-stu-id="96ee0-131">Gets a value indicating whether the stream supports writing.</span></span> <span data-ttu-id="96ee0-132">Esegue l'override di <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream. CanWrite</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-132">(Overrides <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream.CanWrite</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-134"><a href="dn334159(v=exchg.10).md">Itag</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-134"><a href="dn334159(v=exchg.10).md">Itag</a></span></span></td>
<td><span data-ttu-id="96ee0-135">Ottiene o imposta il ITag della colonna.</span><span class="sxs-lookup"><span data-stu-id="96ee0-135">Gets or sets the itag of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-137"><a href="dn334205(v=exchg.10).md">Length</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-137"><a href="dn334205(v=exchg.10).md">Length</a></span></span></td>
<td><span data-ttu-id="96ee0-138">Ottiene la lunghezza corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="96ee0-138">Gets the current length of the stream.</span></span> <span data-ttu-id="96ee0-139">Esegue l'override di <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream. length</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-139">(Overrides <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream.Length</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-141"><a href="dn334161(v=exchg.10).md">Position</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-141"><a href="dn334161(v=exchg.10).md">Position</a></span></span></td>
<td><span data-ttu-id="96ee0-142">Ottiene o imposta la posizione corrente nel flusso.</span><span class="sxs-lookup"><span data-stu-id="96ee0-142">Gets or sets the current position in the stream.</span></span> <span data-ttu-id="96ee0-143">(Esegue l'override di <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream. Position</a>.)</span><span class="sxs-lookup"><span data-stu-id="96ee0-143">(Overrides <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream.Position</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span></span></td>
<td><span data-ttu-id="96ee0-146">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-146">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="96ee0-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span></span></td>
<td><span data-ttu-id="96ee0-149">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-149">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96ee0-150">Inizio</span><span class="sxs-lookup"><span data-stu-id="96ee0-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="96ee0-151">Metodi</span><span class="sxs-lookup"><span data-stu-id="96ee0-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="96ee0-152">Nome</span><span class="sxs-lookup"><span data-stu-id="96ee0-152">Name</span></span></th>
<th><span data-ttu-id="96ee0-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96ee0-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span></span></td>
<td><span data-ttu-id="96ee0-156">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-156">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span></span></td>
<td><span data-ttu-id="96ee0-159">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-159">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span></span></td>
<td><span data-ttu-id="96ee0-162">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-162">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span></span></td>
<td><span data-ttu-id="96ee0-165">Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-165">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="96ee0-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span></span></td>
<td><span data-ttu-id="96ee0-168"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="96ee0-168"><strong>Obsolete.</strong></span></span> <span data-ttu-id="96ee0-169">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-169">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="96ee0-172">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-172">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="96ee0-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (valore booleano)</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="96ee0-175">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-175">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span></span></td>
<td><span data-ttu-id="96ee0-178">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-178">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span></span></td>
<td><span data-ttu-id="96ee0-181">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-181">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="96ee0-184">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-184">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="96ee0-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="96ee0-187">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-187">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-189"><a href="dn334193(v=exchg.10).md">Svuotamento</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-189"><a href="dn334193(v=exchg.10).md">Flush</a></span></span></td>
<td><span data-ttu-id="96ee0-190">Svuotare il flusso.</span><span class="sxs-lookup"><span data-stu-id="96ee0-190">Flush the stream.</span></span> <span data-ttu-id="96ee0-191">Esegue l'override di <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream. Flush ()</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-191">(Overrides <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream.Flush()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="96ee0-194">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-194">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span></span></td>
<td><span data-ttu-id="96ee0-197">Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-197">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="96ee0-200">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-200">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span></span></td>
<td><span data-ttu-id="96ee0-203">Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-203">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="96ee0-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone ()</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></span></span></td>
<td><span data-ttu-id="96ee0-206">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-206">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="96ee0-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (booleano)</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone(Boolean)</a></span></span></td>
<td><span data-ttu-id="96ee0-209">Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-209">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-211"><a href="dn334198(v=exchg.10).md">Lettura</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-211"><a href="dn334198(v=exchg.10).md">Read</a></span></span></td>
<td><span data-ttu-id="96ee0-212">Legge una sequenza di byte dal flusso corrente e fa avanzare la posizione nel flusso del numero di byte letti.</span><span class="sxs-lookup"><span data-stu-id="96ee0-212">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span> <span data-ttu-id="96ee0-213">Esegue l'override di <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream. Read ([], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-213">(Overrides <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream.Read([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span></span></td>
<td><span data-ttu-id="96ee0-216">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-216">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-218"><a href="dn334154(v=exchg.10).md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-218"><a href="dn334154(v=exchg.10).md">Seek</a></span></span></td>
<td><span data-ttu-id="96ee0-219">Imposta la posizione all'interno del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="96ee0-219">Sets the position in the current stream.</span></span> <span data-ttu-id="96ee0-220">(Esegue l'override <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">di Stream. Seek (Int64, SeekOrigin)</a>).</span><span class="sxs-lookup"><span data-stu-id="96ee0-220">(Overrides <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream.Seek(Int64, SeekOrigin)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span></span></td>
<td><span data-ttu-id="96ee0-223">Imposta la lunghezza del flusso.</span><span class="sxs-lookup"><span data-stu-id="96ee0-223">Sets the length of the stream.</span></span> <span data-ttu-id="96ee0-224">Esegue l'override di <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. selength (Int64)</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-224">(Overrides <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream.SetLength(Int64)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-226"><a href="dn334149(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-226"><a href="dn334149(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="96ee0-227">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta l'oggetto <a href="dn334143(v=exchg.10).md">ColumnStream</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="96ee0-227">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn334143(v=exchg.10).md">ColumnStream</a>.</span></span> <span data-ttu-id="96ee0-228">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-228">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-230"><a href="dn334197(v=exchg.10).md">Scrittura</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-230"><a href="dn334197(v=exchg.10).md">Write</a></span></span></td>
<td><span data-ttu-id="96ee0-231">Scrive una sequenza di byte nel flusso corrente e fa avanzare la posizione corrente nel flusso del numero di byte scritti.</span><span class="sxs-lookup"><span data-stu-id="96ee0-231">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span> <span data-ttu-id="96ee0-232">Esegue l'override <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">di Stream. Write ([], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-232">(Overrides <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream.Write([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="96ee0-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span><span class="sxs-lookup"><span data-stu-id="96ee0-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span></span></td>
<td><span data-ttu-id="96ee0-235">Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</span><span class="sxs-lookup"><span data-stu-id="96ee0-235">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96ee0-236">Inizio</span><span class="sxs-lookup"><span data-stu-id="96ee0-236">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="96ee0-237">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96ee0-237">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="96ee0-238">Riferimento</span><span class="sxs-lookup"><span data-stu-id="96ee0-238">Reference</span></span>

[<span data-ttu-id="96ee0-239">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="96ee0-239">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="96ee0-240">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="96ee0-240">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
