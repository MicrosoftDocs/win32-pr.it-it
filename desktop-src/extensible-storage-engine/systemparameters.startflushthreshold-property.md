---
description: 'Altre informazioni su: Proprietà SystemParameters. StartFlushThreshold'
title: Proprietà SystemParameters. StartFlushThreshold
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347971"
---
# <a name="systemparametersstartflushthreshold-property"></a><span data-ttu-id="c2567-103">Proprietà SystemParameters. StartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="c2567-103">SystemParameters.StartFlushThreshold property</span></span>

<span data-ttu-id="c2567-104">Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database inizia a rimuovere le pagine dalla cache per creare spazio per le pagine che non sono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="c2567-104">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="c2567-105">Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, viene avviato un processo in background per ripristinare il pool di buffer disponibili.</span><span class="sxs-lookup"><span data-stu-id="c2567-105">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="c2567-106">Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="c2567-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="c2567-107">Anche questa soglia deve essere sempre inferiore alla soglia di arresto impostata dal JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="c2567-107">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="c2567-108">L'altezza della distanza della soglia iniziale determina il tempo di risposta che la cache delle pagine del database deve avere per produrre i buffer disponibili prima che siano necessari per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2567-108">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="c2567-109">Una soglia di inizio elevata offrirà al processo in background più tempo per rispondere.</span><span class="sxs-lookup"><span data-stu-id="c2567-109">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="c2567-110">Tuttavia, una soglia di avvio elevata implica una soglia di arresto superiore e che ridurrà le dimensioni effettive della cache delle pagine del database.</span><span class="sxs-lookup"><span data-stu-id="c2567-110">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="c2567-111">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c2567-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c2567-112">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c2567-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c2567-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2567-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c2567-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c2567-114">Property value</span></span>

<span data-ttu-id="c2567-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c2567-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2567-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2567-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c2567-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c2567-117">Reference</span></span>

[<span data-ttu-id="c2567-118">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="c2567-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="c2567-119">Membri SystemParameters</span><span class="sxs-lookup"><span data-stu-id="c2567-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="c2567-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c2567-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
