---
description: 'Altre informazioni su: metodo API. JetReadFileInstance'
title: API. JetReadFileInstance, metodo
TOCTitle: 'JetReadFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetreadfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100781
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80eaf61fd9cd07fce80d32fddf7056f6bff683c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318476"
---
# <a name="apijetreadfileinstance-method"></a><span data-ttu-id="18c90-103">API. JetReadFileInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="18c90-103">Api.JetReadFileInstance method</span></span>

<span data-ttu-id="18c90-104">Recupera il contenuto di un file aperto con [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="18c90-104">Retrieves the contents of a file opened with [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span></span>

<span data-ttu-id="18c90-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="18c90-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="18c90-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="18c90-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="18c90-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18c90-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetReadFileInstance ( _
    instance As JET_INSTANCE, _
    file As JET_HANDLE, _
    buffer As Byte(), _
    bufferSize As Integer, _
    <OutAttribute> ByRef bytesRead As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As JET_HANDLE
Dim buffer As Byte()
Dim bufferSize As Integer
Dim bytesRead As IntegerApi.JetReadFileInstance(instance, _
    file, buffer, bufferSize, bytesRead)
```

``` csharp
public static void JetReadFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE file,
    byte[] buffer,
    int bufferSize,
    out int bytesRead
)
```

#### <a name="parameters"></a><span data-ttu-id="18c90-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="18c90-108">Parameters</span></span>

  - <span data-ttu-id="18c90-109">instance</span><span class="sxs-lookup"><span data-stu-id="18c90-109">instance</span></span>  
    <span data-ttu-id="18c90-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="18c90-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="18c90-111">Istanza di da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="18c90-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="18c90-112">file</span><span class="sxs-lookup"><span data-stu-id="18c90-112">file</span></span>  
    <span data-ttu-id="18c90-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="18c90-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="18c90-114">File da cui eseguire la lettura.</span><span class="sxs-lookup"><span data-stu-id="18c90-114">The file to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="18c90-115">buffer</span><span class="sxs-lookup"><span data-stu-id="18c90-115">buffer</span></span>  
    <span data-ttu-id="18c90-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="18c90-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="18c90-117">Buffer in cui leggere.</span><span class="sxs-lookup"><span data-stu-id="18c90-117">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="18c90-118">bufferSize</span><span class="sxs-lookup"><span data-stu-id="18c90-118">bufferSize</span></span>  
    <span data-ttu-id="18c90-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="18c90-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="18c90-120">Dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="18c90-120">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="18c90-121">bytesRead</span><span class="sxs-lookup"><span data-stu-id="18c90-121">bytesRead</span></span>  
    <span data-ttu-id="18c90-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="18c90-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="18c90-123">Restituisce la quantità di dati letti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="18c90-123">Returns the amount of data read into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="18c90-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18c90-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="18c90-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="18c90-125">Reference</span></span>

[<span data-ttu-id="18c90-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="18c90-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="18c90-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="18c90-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="18c90-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="18c90-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
