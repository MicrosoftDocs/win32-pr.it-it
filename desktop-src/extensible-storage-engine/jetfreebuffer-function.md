---
description: 'Altre informazioni su: funzione JetFreeBuffer'
title: JetFreeBuffer (funzione)
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317344"
---
# <a name="jetfreebuffer-function"></a><span data-ttu-id="3a4f5-103">JetFreeBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="3a4f5-103">JetFreeBuffer Function</span></span>


<span data-ttu-id="3a4f5-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3a4f5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetfreebuffer-function"></a><span data-ttu-id="3a4f5-105">JetFreeBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="3a4f5-105">JetFreeBuffer Function</span></span>

<span data-ttu-id="3a4f5-106">La funzione **JetFreeBuffer** libera la memoria allocata da una chiamata al motore di database.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-106">The **JetFreeBuffer** function frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="3a4f5-107">**Windows XP: JetFreeBuffer** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-107">**Windows XP:  JetFreeBuffer** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a><span data-ttu-id="3a4f5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a4f5-108">Parameters</span></span>

<span data-ttu-id="3a4f5-109">*pbBuf*</span><span class="sxs-lookup"><span data-stu-id="3a4f5-109">*pbBuf*</span></span>

<span data-ttu-id="3a4f5-110">Puntatore a un'area di memoria allocata in precedenza da una chiamata al motore di database.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-110">Pointer to a region of memory that was previously allocated by a call to the database engine.</span></span> <span data-ttu-id="3a4f5-111">Il **valore null** è accettabile e verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-111">**NULL** is acceptable, and will be ignored.</span></span>

### <a name="return-value"></a><span data-ttu-id="3a4f5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a4f5-112">Return Value</span></span>

<span data-ttu-id="3a4f5-113">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3a4f5-114">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3a4f5-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a4f5-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3a4f5-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="3a4f5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a4f5-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a4f5-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3a4f5-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3a4f5-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="3a4f5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a4f5-119">Remarks</span></span>

<span data-ttu-id="3a4f5-120">Si tratta di un comportamento non definito che consente di passare memoria non allocata dal motore di database in a *pbBuf*.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-120">It is undefined behavior to pass memory that was not allocated by the database engine in to *pbBuf*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3a4f5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a4f5-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a4f5-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3a4f5-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4f5-123">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-123">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4f5-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3a4f5-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4f5-125">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-125">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4f5-126"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3a4f5-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4f5-127">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4f5-128"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="3a4f5-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4f5-129">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4f5-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3a4f5-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4f5-131">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3a4f5-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3a4f5-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3a4f5-132">See Also</span></span>

[<span data-ttu-id="3a4f5-133">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3a4f5-133">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3a4f5-134">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="3a4f5-134">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)
