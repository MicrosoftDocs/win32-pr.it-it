---
description: 'Altre informazioni su: funzione JetGetVersion'
title: JetGetVersion (funzione)
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38128358d814ea85cf087c270a65a3fada976e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233637"
---
# <a name="jetgetversion-function"></a><span data-ttu-id="3c0c7-103">JetGetVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c0c7-103">JetGetVersion Function</span></span>


<span data-ttu-id="3c0c7-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3c0c7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetversion-function"></a><span data-ttu-id="3c0c7-105">JetGetVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c0c7-105">JetGetVersion Function</span></span>

<span data-ttu-id="3c0c7-106">La funzione **JetGetVersion** recupera la versione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-106">The **JetGetVersion** function retrieves the version of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a><span data-ttu-id="3c0c7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c0c7-107">Parameters</span></span>

<span data-ttu-id="3c0c7-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3c0c7-108">*sesid*</span></span>

<span data-ttu-id="3c0c7-109">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-109">The session to use for this call.</span></span>

<span data-ttu-id="3c0c7-110">*pwVersion*</span><span class="sxs-lookup"><span data-stu-id="3c0c7-110">*pwVersion*</span></span>

<span data-ttu-id="3c0c7-111">Puntatore al numero di versione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-111">A pointer to the version number of the database engine.</span></span>

### <a name="return-value"></a><span data-ttu-id="3c0c7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c0c7-112">Return Value</span></span>

<span data-ttu-id="3c0c7-113">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3c0c7-114">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3c0c7-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c0c7-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3c0c7-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="3c0c7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c0c7-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c0c7-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3c0c7-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3c0c7-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3c0c7-119">Se questa funzione ha esito positivo, viene recuperata la versione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-119">If this function succeeds, the version of the database engine is retrieved.</span></span>

<span data-ttu-id="3c0c7-120">Non sono presenti modalità di errore note.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-120">There are no known failure modes.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3c0c7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c0c7-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c0c7-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3c0c7-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3c0c7-123">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c0c7-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3c0c7-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3c0c7-125">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c0c7-126"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3c0c7-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3c0c7-127">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c0c7-128"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="3c0c7-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3c0c7-129">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c0c7-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3c0c7-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3c0c7-131">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3c0c7-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3c0c7-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c0c7-132">See Also</span></span>

[<span data-ttu-id="3c0c7-133">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="3c0c7-133">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="3c0c7-134">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="3c0c7-134">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="3c0c7-135">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3c0c7-135">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3c0c7-136">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3c0c7-136">JET_SESID</span></span>](./jet-sesid.md)
