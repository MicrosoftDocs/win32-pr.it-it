---
description: 'Altre informazioni su: metodo API. JetGetLogInfoInstance'
title: API. JetGetLogInfoInstance, metodo
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85e252b74c47d3274fc83af59e3fb571906219fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306277"
---
# <a name="apijetgetloginfoinstance-method"></a><span data-ttu-id="6b649-103">API. JetGetLogInfoInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="6b649-103">Api.JetGetLogInfoInstance method</span></span>

<span data-ttu-id="6b649-104">Usato durante un backup avviato da [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) per eseguire una query su un'istanza per i nomi dei file di patch del database e i file di log che devono diventare parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="6b649-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database patch files and logfiles that should become part of the backup file set.</span></span> <span data-ttu-id="6b649-105">Questi file possono essere successivamente aperti usando [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) e read using [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="6b649-105">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="6b649-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6b649-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6b649-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6b649-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b649-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b649-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="6b649-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b649-109">Parameters</span></span>

  - <span data-ttu-id="6b649-110">instance</span><span class="sxs-lookup"><span data-stu-id="6b649-110">instance</span></span>  
    <span data-ttu-id="6b649-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6b649-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="6b649-112">Istanza per cui ottenere le informazioni.</span><span class="sxs-lookup"><span data-stu-id="6b649-112">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b649-113">files</span><span class="sxs-lookup"><span data-stu-id="6b649-113">files</span></span>  
    <span data-ttu-id="6b649-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6b649-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6b649-115">Restituisce un elenco di stringhe con terminazione null che descrivono il set di file di patch del database e file di log che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="6b649-115">Returns a list of null terminated strings describing the set of database patch files and log files that should be a part of the backup file set.</span></span> <span data-ttu-id="6b649-116">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6b649-116">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="6b649-117">Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="6b649-117">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b649-118">maxChars</span><span class="sxs-lookup"><span data-stu-id="6b649-118">maxChars</span></span>  
    <span data-ttu-id="6b649-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6b649-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6b649-120">Numero massimo di caratteri da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6b649-120">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b649-121">actualChars</span><span class="sxs-lookup"><span data-stu-id="6b649-121">actualChars</span></span>  
    <span data-ttu-id="6b649-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6b649-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6b649-123">Dimensioni effettive dell'elenco dei file.</span><span class="sxs-lookup"><span data-stu-id="6b649-123">Actual size of the file list.</span></span> <span data-ttu-id="6b649-124">Se è maggiore di maxChars, l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="6b649-124">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b649-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b649-125">Remarks</span></span>

<span data-ttu-id="6b649-126">È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="6b649-126">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b649-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b649-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6b649-128">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6b649-128">Reference</span></span>

[<span data-ttu-id="6b649-129">Classe API</span><span class="sxs-lookup"><span data-stu-id="6b649-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6b649-130">Membri API</span><span class="sxs-lookup"><span data-stu-id="6b649-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6b649-131">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6b649-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
