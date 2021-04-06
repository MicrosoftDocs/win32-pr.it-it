---
description: 'Altre informazioni su: Proprietà JET_RETRIEVECOLUMN'
title: Proprietà JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758507"
---
# <a name="jet_retrievecolumn-properties"></a><span data-ttu-id="ef43d-103">Proprietà JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="ef43d-103">JET_RETRIEVECOLUMN properties</span></span>

<span data-ttu-id="ef43d-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="ef43d-104">Include protected members</span></span>  
<span data-ttu-id="ef43d-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="ef43d-105">Include inherited members</span></span>  

<span data-ttu-id="ef43d-106">Il tipo di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ef43d-106">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="ef43d-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef43d-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ef43d-108">Nome</span><span class="sxs-lookup"><span data-stu-id="ef43d-108">Name</span></span></th>
<th><span data-ttu-id="ef43d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef43d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="ef43d-112">Ottiene la dimensione, in byte, dei dati recuperati da un'operazione di recupero colonna.</span><span class="sxs-lookup"><span data-stu-id="ef43d-112">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-114"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-114"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="ef43d-115">Ottiene o imposta le dimensioni in byte del buffer <a href="dn351040(v=exchg.10).md">pvData</a> .</span><span class="sxs-lookup"><span data-stu-id="ef43d-115">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="ef43d-116">Tramite l'operazione di recupero colonna non vengono archiviati più dati in pvData rispetto a cbData.</span><span class="sxs-lookup"><span data-stu-id="ef43d-116">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-118"><a href="dn335230(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-118"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="ef43d-119">Ottiene o imposta l'identificatore di colonna per la colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ef43d-119">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="ef43d-122">Ottiene l'ColumnID della colonna contrassegnata, multivalore o di tipo sparse quando tutte le colonne con tag vengono recuperate passando 0 come ColumnID.</span><span class="sxs-lookup"><span data-stu-id="ef43d-122">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-124"><a href="dn335231(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-124"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="ef43d-125">Ottiene l'avviso restituito dal recupero della colonna.</span><span class="sxs-lookup"><span data-stu-id="ef43d-125">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-127"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-127"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="ef43d-128">Ottiene o imposta le opzioni per il recupero della colonna.</span><span class="sxs-lookup"><span data-stu-id="ef43d-128">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-130"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-130"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="ef43d-131">Ottiene o imposta l'offset nel buffer in cui verranno archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="ef43d-131">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="ef43d-134">Ottiene o imposta l'offset del primo byte da recuperare da una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="ef43d-134">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="ef43d-137">Ottiene o imposta il numero di sequenza dei valori contenuti in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="ef43d-137">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="ef43d-138">Se itagSequence è 0, viene restituito il numero di istanze di una colonna multivalore anziché dati di colonna.</span><span class="sxs-lookup"><span data-stu-id="ef43d-138">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="ef43d-140"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="ef43d-140"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="ef43d-141">Ottiene o imposta il buffer in cui vengono archiviati i dati recuperati dalla colonna.</span><span class="sxs-lookup"><span data-stu-id="ef43d-141">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef43d-142">Inizio</span><span class="sxs-lookup"><span data-stu-id="ef43d-142">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ef43d-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef43d-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef43d-144">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ef43d-144">Reference</span></span>

[<span data-ttu-id="ef43d-145">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="ef43d-145">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="ef43d-146">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ef43d-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
