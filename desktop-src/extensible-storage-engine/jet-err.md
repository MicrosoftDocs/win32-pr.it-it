---
description: 'Altre informazioni su: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323780"
---
# <a name="jet_err"></a><span data-ttu-id="35d37-103">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35d37-103">JET_ERR</span></span>


<span data-ttu-id="35d37-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="35d37-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_err"></a><span data-ttu-id="35d37-105">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35d37-105">JET_ERR</span></span>

<span data-ttu-id="35d37-106">Il tipo di dati **JET_ERR** contiene un [codice di errore del motore di archiviazione estensibile](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="35d37-106">The **JET_ERR** data type contains an [Extensible Storage Engine error code](./extensible-storage-engine-error-codes.md).</span></span>

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a><span data-ttu-id="35d37-107">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="35d37-107">Data Types</span></span>

<span data-ttu-id="35d37-108">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35d37-108">JET_ERR</span></span>

<span data-ttu-id="35d37-109">Un valore zero (corrispondente a JET_errSuccess) indica che la chiamata ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="35d37-109">A zero value (corresponding to JET_errSuccess) indicates that the call succeeded.</span></span> <span data-ttu-id="35d37-110">Un valore positivo avverte una condizione non irreversibile che si è verificata durante una chiamata altrimenti riuscita.</span><span class="sxs-lookup"><span data-stu-id="35d37-110">A positive value warns of a non-fatal condition that occurred during an otherwise successful call.</span></span> <span data-ttu-id="35d37-111">Un valore negativo indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="35d37-111">A negative value indicates that the call failed.</span></span>

### <a name="remarks"></a><span data-ttu-id="35d37-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="35d37-112">Remarks</span></span>

<span data-ttu-id="35d37-113">Per informazioni sulla restituzione di errori come HRESULT, vedere [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="35d37-113">For information about returning errors as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="35d37-114">Per informazioni sui flag per la configurazione del database per la gestione degli errori, vedere la pagina relativa ai [parametri di gestione degli](./error-handling-parameters.md)errori.</span><span class="sxs-lookup"><span data-stu-id="35d37-114">For information about flags for configuring the database to handle errors, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="35d37-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35d37-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35d37-116"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="35d37-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="35d37-117">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="35d37-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35d37-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="35d37-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="35d37-119">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="35d37-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35d37-120"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="35d37-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="35d37-121">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="35d37-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="35d37-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="35d37-122">See Also</span></span>

[<span data-ttu-id="35d37-123">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="35d37-123">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="35d37-124">Codici di errore di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="35d37-124">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="35d37-125">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="35d37-125">Error Handling Parameters</span></span>](./error-handling-parameters.md)
