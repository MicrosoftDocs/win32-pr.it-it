---
description: 'Altre informazioni su: metodo API. JetGetTruncateLogInfoInstance'
title: API. JetGetTruncateLogInfoInstance, metodo
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233975"
---
# <a name="apijetgettruncateloginfoinstance-method"></a><span data-ttu-id="7da8f-103">API. JetGetTruncateLogInfoInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="7da8f-103">Api.JetGetTruncateLogInfoInstance method</span></span>

<span data-ttu-id="7da8f-104">Utilizzato durante un backup avviato da [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) per eseguire una query su un'istanza di per i nomi dei file di log delle transazioni che possono essere eliminati in modo sicuro dopo il completamento del backup.</span><span class="sxs-lookup"><span data-stu-id="7da8f-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="7da8f-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7da8f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7da8f-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7da8f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7da8f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7da8f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="7da8f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7da8f-108">Parameters</span></span>

  - <span data-ttu-id="7da8f-109">instance</span><span class="sxs-lookup"><span data-stu-id="7da8f-109">instance</span></span>  
    <span data-ttu-id="7da8f-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7da8f-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7da8f-111">Istanza per cui ottenere le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7da8f-111">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="7da8f-112">files</span><span class="sxs-lookup"><span data-stu-id="7da8f-112">files</span></span>  
    <span data-ttu-id="7da8f-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7da8f-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7da8f-114">Restituisce un elenco di stringhe con terminazione null che descrivono il set di file di log del database che possono essere eliminati in modo sicuro al termine del backup.</span><span class="sxs-lookup"><span data-stu-id="7da8f-114">Returns a list of null terminated strings describing the set of database log files that can be safely deleted after the backup completes.</span></span> <span data-ttu-id="7da8f-115">L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7da8f-115">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="7da8f-116">Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.</span><span class="sxs-lookup"><span data-stu-id="7da8f-116">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="7da8f-117">maxChars</span><span class="sxs-lookup"><span data-stu-id="7da8f-117">maxChars</span></span>  
    <span data-ttu-id="7da8f-118">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7da8f-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7da8f-119">Numero massimo di caratteri da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7da8f-119">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="7da8f-120">actualChars</span><span class="sxs-lookup"><span data-stu-id="7da8f-120">actualChars</span></span>  
    <span data-ttu-id="7da8f-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7da8f-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7da8f-122">Dimensioni effettive dell'elenco dei file.</span><span class="sxs-lookup"><span data-stu-id="7da8f-122">Actual size of the file list.</span></span> <span data-ttu-id="7da8f-123">Se è maggiore di maxChars, l'elenco è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="7da8f-123">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="7da8f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="7da8f-124">Remarks</span></span>

<span data-ttu-id="7da8f-125">È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="7da8f-125">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="7da8f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7da8f-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7da8f-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7da8f-127">Reference</span></span>

[<span data-ttu-id="7da8f-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="7da8f-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7da8f-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="7da8f-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7da8f-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7da8f-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
