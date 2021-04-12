---
description: 'Altre informazioni su: Proprietà SystemParameters. StopFlushThreshold'
title: Proprietà SystemParameters. StopFlushThreshold
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347966"
---
# <a name="systemparametersstopflushthreshold-property"></a><span data-ttu-id="4e24b-103">Proprietà SystemParameters. StopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="4e24b-103">SystemParameters.StopFlushThreshold property</span></span>

<span data-ttu-id="4e24b-104">Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database smette di rimuovere le pagine dalla cache per creare spazio per le pagine non memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="4e24b-104">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="4e24b-105">Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background che è stato avviato per ripristinare il pool di buffer disponibili viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="4e24b-105">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="4e24b-106">Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="4e24b-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="4e24b-107">Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata da JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="4e24b-107">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="4e24b-108">La distanza tra la soglia iniziale e la soglia di arresto influiscono sull'efficienza con cui le pagine del database vengono scaricate dal processo in background.</span><span class="sxs-lookup"><span data-stu-id="4e24b-108">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="4e24b-109">Un gap maggiore renderà più probabile che le Scritture nelle pagine adiacenti vengano combinate.</span><span class="sxs-lookup"><span data-stu-id="4e24b-109">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="4e24b-110">Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="4e24b-110">However, a high stop threshold will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="4e24b-111">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4e24b-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4e24b-112">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4e24b-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e24b-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e24b-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4e24b-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4e24b-114">Property value</span></span>

<span data-ttu-id="4e24b-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4e24b-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4e24b-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e24b-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4e24b-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4e24b-117">Reference</span></span>

[<span data-ttu-id="4e24b-118">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="4e24b-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="4e24b-119">Membri SystemParameters</span><span class="sxs-lookup"><span data-stu-id="4e24b-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="4e24b-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4e24b-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
