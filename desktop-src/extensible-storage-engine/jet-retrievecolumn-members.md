---
description: 'Altre informazioni su: membri JET_RETRIEVECOLUMN'
title: Membri JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555439"
---
# <a name="jet_retrievecolumn-members"></a><span data-ttu-id="8dd3b-103">Membri JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="8dd3b-103">JET_RETRIEVECOLUMN members</span></span>

<span data-ttu-id="8dd3b-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="8dd3b-104">Include protected members</span></span>  
<span data-ttu-id="8dd3b-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="8dd3b-105">Include inherited members</span></span>  

<span data-ttu-id="8dd3b-106">Contiene i parametri di input e output per [JetRetrieveColumns (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetretrievecolumns-method.md).</span><span class="sxs-lookup"><span data-stu-id="8dd3b-106">Contains input and output parameters for [JetRetrieveColumns(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetretrievecolumns-method.md).</span></span> <span data-ttu-id="8dd3b-107">I campi della struttura descrivono il valore della colonna da recuperare, il modo in cui recuperarlo e il percorso in cui salvare i risultati.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

<span data-ttu-id="8dd3b-108">Il tipo di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-108">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="8dd3b-109">Costruttori</span><span class="sxs-lookup"><span data-stu-id="8dd3b-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8dd3b-110">Nome</span><span class="sxs-lookup"><span data-stu-id="8dd3b-110">Name</span></span></th>
<th><span data-ttu-id="8dd3b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd3b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="8dd3b-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8dd3b-114">Inizio</span><span class="sxs-lookup"><span data-stu-id="8dd3b-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="8dd3b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8dd3b-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8dd3b-116">Nome</span><span class="sxs-lookup"><span data-stu-id="8dd3b-116">Name</span></span></th>
<th><span data-ttu-id="8dd3b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd3b-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="8dd3b-120">Ottiene la dimensione, in byte, dei dati recuperati da un'operazione di recupero colonna.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-120">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-122"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-122"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="8dd3b-123">Ottiene o imposta le dimensioni in byte del buffer <a href="dn351040(v=exchg.10).md">pvData</a> .</span><span class="sxs-lookup"><span data-stu-id="8dd3b-123">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="8dd3b-124">Tramite l'operazione di recupero colonna non vengono archiviati più dati in pvData rispetto a cbData.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-124">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-126"><a href="dn335230(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-126"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="8dd3b-127">Ottiene o imposta l'identificatore di colonna per la colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-127">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="8dd3b-130">Ottiene l'ColumnID della colonna contrassegnata, multivalore o di tipo sparse quando tutte le colonne con tag vengono recuperate passando 0 come ColumnID.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-130">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-132"><a href="dn335231(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-132"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="8dd3b-133">Ottiene l'avviso restituito dal recupero della colonna.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-133">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-135"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-135"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="8dd3b-136">Ottiene o imposta le opzioni per il recupero della colonna.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-136">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-138"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-138"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="8dd3b-139">Ottiene o imposta l'offset nel buffer in cui verranno archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-139">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="8dd3b-142">Ottiene o imposta l'offset del primo byte da recuperare da una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-142">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="8dd3b-145">Ottiene o imposta il numero di sequenza dei valori contenuti in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-145">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="8dd3b-146">Se itagSequence è 0, viene restituito il numero di istanze di una colonna multivalore anziché dati di colonna.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-146">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8dd3b-148"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-148"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="8dd3b-149">Ottiene o imposta il buffer in cui vengono archiviati i dati recuperati dalla colonna.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-149">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8dd3b-150">Inizio</span><span class="sxs-lookup"><span data-stu-id="8dd3b-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="8dd3b-151">Metodi</span><span class="sxs-lookup"><span data-stu-id="8dd3b-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8dd3b-152">Nome</span><span class="sxs-lookup"><span data-stu-id="8dd3b-152">Name</span></span></th>
<th><span data-ttu-id="8dd3b-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd3b-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="8dd3b-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="8dd3b-156">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-156">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="8dd3b-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="8dd3b-159">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="8dd3b-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="8dd3b-162">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="8dd3b-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="8dd3b-165">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="8dd3b-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="8dd3b-168">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-168">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="8dd3b-170"><a href="dn335224(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="8dd3b-170"><a href="dn335224(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="8dd3b-171">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-171">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>.</span></span> <span data-ttu-id="8dd3b-172">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="8dd3b-172">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8dd3b-173">Inizio</span><span class="sxs-lookup"><span data-stu-id="8dd3b-173">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="8dd3b-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dd3b-174">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dd3b-175">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8dd3b-175">Reference</span></span>

[<span data-ttu-id="8dd3b-176">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="8dd3b-176">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="8dd3b-177">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8dd3b-177">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
