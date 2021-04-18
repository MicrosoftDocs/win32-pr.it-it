---
description: 'Altre informazioni su: Enumerazione RetrieveColumnGrbit'
title: Enumerazione RetrieveColumnGrbit
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313077"
---
# <a name="retrievecolumngrbit-enumeration"></a><span data-ttu-id="3318f-103">Enumerazione RetrieveColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="3318f-103">RetrieveColumnGrbit enumeration</span></span>

<span data-ttu-id="3318f-104">Opzioni per JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="3318f-104">Options for JetRetrieveColumn.</span></span>

<span data-ttu-id="3318f-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="3318f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3318f-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3318f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3318f-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3318f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3318f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3318f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a><span data-ttu-id="3318f-109">Members</span><span class="sxs-lookup"><span data-stu-id="3318f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3318f-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="3318f-110">Member name</span></span></th>
<th><span data-ttu-id="3318f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3318f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3318f-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="3318f-112">None</span></span></td>
<td><span data-ttu-id="3318f-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="3318f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3318f-114">RetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="3318f-114">RetrieveCopy</span></span></td>
<td><span data-ttu-id="3318f-115">Questo flag consente a retrieve Column di recuperare il valore modificato anziché il valore originale.</span><span class="sxs-lookup"><span data-stu-id="3318f-115">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="3318f-116">Se il valore non è stato modificato, viene recuperato il valore originale.</span><span class="sxs-lookup"><span data-stu-id="3318f-116">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="3318f-117">In questo modo, è possibile recuperare un valore che non è ancora stato inserito o aggiornato durante l'operazione di inserimento o aggiornamento di un record.</span><span class="sxs-lookup"><span data-stu-id="3318f-117">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3318f-118">RetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="3318f-118">RetrieveFromIndex</span></span></td>
<td><span data-ttu-id="3318f-119">Questa opzione viene utilizzata per recuperare i valori di colonna dall'indice, se possibile, senza accedere al record.</span><span class="sxs-lookup"><span data-stu-id="3318f-119">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="3318f-120">In questo modo, è possibile evitare il caricamento di record superflui quando sono disponibili dati necessari dalle voci dell'indice.</span><span class="sxs-lookup"><span data-stu-id="3318f-120">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3318f-121">RetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="3318f-121">RetrieveFromPrimaryBookmark</span></span></td>
<td><span data-ttu-id="3318f-122">Questa opzione viene utilizzata per recuperare i valori di colonna dal segnalibro index e può variare dal valore di indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="3318f-122">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="3318f-123">Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario.</span><span class="sxs-lookup"><span data-stu-id="3318f-123">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="3318f-124">Non è possibile impostare questo bit se è stato impostato anche RetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="3318f-124">This bit cannot be set if RetrieveFromIndex is also set.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3318f-125">RetrieveTag</span><span class="sxs-lookup"><span data-stu-id="3318f-125">RetrieveTag</span></span></td>
<td><span data-ttu-id="3318f-126">Questa opzione viene utilizzata per recuperare il numero di sequenza di un valore di colonna multivalore in JET_RETINFO. itagSequence.</span><span class="sxs-lookup"><span data-stu-id="3318f-126">This option is used to retrieve the sequence number of a multi-valued column value in JET_RETINFO.itagSequence.</span></span> <span data-ttu-id="3318f-127">Il recupero del numero di sequenza può essere un'operazione costosa e deve essere eseguito solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="3318f-127">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3318f-128">RetrieveNull</span><span class="sxs-lookup"><span data-stu-id="3318f-128">RetrieveNull</span></span></td>
<td><span data-ttu-id="3318f-129">Questa opzione viene utilizzata per recuperare i valori NULL della colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="3318f-129">This option is used to retrieve multi-valued column NULL values.</span></span> <span data-ttu-id="3318f-130">Se questa opzione non è specificata, i valori NULL della colonna multivalore verranno automaticamente ignorati.</span><span class="sxs-lookup"><span data-stu-id="3318f-130">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3318f-131">RetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="3318f-131">RetrieveIgnoreDefault</span></span></td>
<td><span data-ttu-id="3318f-132">Questa opzione ha effetto solo sulle colonne multivalore e causa la restituzione di un valore NULL quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record.</span><span class="sxs-lookup"><span data-stu-id="3318f-132">This option affects only multi-valued columns and causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3318f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3318f-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3318f-134">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3318f-134">Reference</span></span>

[<span data-ttu-id="3318f-135">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3318f-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
