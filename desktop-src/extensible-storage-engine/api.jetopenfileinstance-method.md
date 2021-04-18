---
description: 'Altre informazioni su: metodo API. JetOpenFileInstance'
title: API. JetOpenFileInstance, metodo
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318479"
---
# <a name="apijetopenfileinstance-method"></a><span data-ttu-id="7bd1f-103">API. JetOpenFileInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="7bd1f-103">Api.JetOpenFileInstance method</span></span>

<span data-ttu-id="7bd1f-104">Apre un database collegato, un file di patch del database o un file di log delle transazioni di un'istanza attiva allo scopo di eseguire un backup fuzzy di streaming.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-104">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="7bd1f-105">I dati di questi file possono essere successivamente letti tramite l'handle restituito mediante JetReadFileInstance.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-105">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="7bd1f-106">L'handle restituito deve essere chiuso utilizzando JetCloseFileInstance.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-106">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="7bd1f-107">È necessario che un backup esterno dell'istanza sia stato avviato in precedenza utilizzando JetBeginExternalBackupInstance.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-107">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span>

<span data-ttu-id="7bd1f-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7bd1f-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7bd1f-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7bd1f-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd1f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bd1f-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a><span data-ttu-id="7bd1f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bd1f-111">Parameters</span></span>

  - <span data-ttu-id="7bd1f-112">instance</span><span class="sxs-lookup"><span data-stu-id="7bd1f-112">instance</span></span>  
    <span data-ttu-id="7bd1f-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7bd1f-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7bd1f-114">Istanza di da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-114">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7bd1f-115">file</span><span class="sxs-lookup"><span data-stu-id="7bd1f-115">file</span></span>  
    <span data-ttu-id="7bd1f-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7bd1f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7bd1f-117">File da aprire.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-117">The file to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="7bd1f-118">gestire</span><span class="sxs-lookup"><span data-stu-id="7bd1f-118">handle</span></span>  
    <span data-ttu-id="7bd1f-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7bd1f-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="7bd1f-120">Restituisce un handle per il file.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-120">Returns a handle to the file.</span></span>

<!-- end list -->

  - <span data-ttu-id="7bd1f-121">fileSizeLow</span><span class="sxs-lookup"><span data-stu-id="7bd1f-121">fileSizeLow</span></span>  
    <span data-ttu-id="7bd1f-122">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="7bd1f-122">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="7bd1f-123">Restituisce i 32 bit meno significativi della dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-123">Returns the least significant 32 bits of the file size.</span></span>

<!-- end list -->

  - <span data-ttu-id="7bd1f-124">fileSizeHigh</span><span class="sxs-lookup"><span data-stu-id="7bd1f-124">fileSizeHigh</span></span>  
    <span data-ttu-id="7bd1f-125">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="7bd1f-125">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="7bd1f-126">Restituisce i 32 bit più significativi della dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="7bd1f-126">Returns the most significant 32 bits of the file size.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bd1f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bd1f-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7bd1f-128">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7bd1f-128">Reference</span></span>

[<span data-ttu-id="7bd1f-129">Classe API</span><span class="sxs-lookup"><span data-stu-id="7bd1f-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7bd1f-130">Membri API</span><span class="sxs-lookup"><span data-stu-id="7bd1f-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7bd1f-131">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7bd1f-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
