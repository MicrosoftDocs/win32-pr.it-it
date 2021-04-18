---
description: 'Altre informazioni su: metodo API. JetGetAttachInfoInstance'
title: API. JetGetAttachInfoInstance, metodo
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306298"
---
# <a name="apijetgetattachinfoinstance-method"></a><span data-ttu-id="7ae59-103">API. JetGetAttachInfoInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="7ae59-103">Api.JetGetAttachInfoInstance method</span></span>

<span data-ttu-id="7ae59-104">Utilizzato durante un backup avviato da [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) per eseguire una query su un'istanza di per i nomi dei file di database che devono diventare parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="7ae59-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="7ae59-105">Verranno considerati solo i database attualmente collegati all'istanza tramite [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae59-105">Only databases that are currently attached to the instance using [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will be considered.</span></span> <span data-ttu-id="7ae59-106">Questi file possono essere successivamente aperti usando [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) e read using [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="7ae59-106">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="7ae59-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7ae59-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7ae59-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7ae59-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae59-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ae59-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="7ae59-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ae59-110">Parameters</span></span>

  - <span data-ttu-id="7ae59-111">instance</span><span class="sxs-lookup"><span data-stu-id="7ae59-111">instance</span></span>  
    <span data-ttu-id="7ae59-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7ae59-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7ae59-113">Istanza per cui ottenere le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7ae59-113">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae59-114">files</span><span class="sxs-lookup"><span data-stu-id="7ae59-114">files</span></span>  
    <span data-ttu-id="7ae59-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7ae59-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7ae59-116">Restituisce un elenco di stringhe con terminazione null che descrivono il set di file di database che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="7ae59-116">Returns a list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="7ae59-117">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ae59-117">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="7ae59-118">Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="7ae59-118">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae59-119">maxChars</span><span class="sxs-lookup"><span data-stu-id="7ae59-119">maxChars</span></span>  
    <span data-ttu-id="7ae59-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7ae59-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7ae59-121">Numero massimo di caratteri da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7ae59-121">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ae59-122">actualChars</span><span class="sxs-lookup"><span data-stu-id="7ae59-122">actualChars</span></span>  
    <span data-ttu-id="7ae59-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7ae59-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7ae59-124">Dimensioni effettive dell'elenco dei file.</span><span class="sxs-lookup"><span data-stu-id="7ae59-124">Actual size of the file list.</span></span> <span data-ttu-id="7ae59-125">Se è maggiore di maxChars, l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="7ae59-125">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae59-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ae59-126">Remarks</span></span>

<span data-ttu-id="7ae59-127">È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="7ae59-127">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ae59-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ae59-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ae59-129">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7ae59-129">Reference</span></span>

[<span data-ttu-id="7ae59-130">Classe API</span><span class="sxs-lookup"><span data-stu-id="7ae59-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7ae59-131">Membri API</span><span class="sxs-lookup"><span data-stu-id="7ae59-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7ae59-132">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7ae59-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
