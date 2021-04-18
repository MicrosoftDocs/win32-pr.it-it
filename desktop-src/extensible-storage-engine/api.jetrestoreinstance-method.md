---
description: 'Altre informazioni su: metodo API. JetRestoreInstance'
title: API. JetRestoreInstance, metodo
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306271"
---
# <a name="apijetrestoreinstance-method"></a><span data-ttu-id="36cd6-103">API. JetRestoreInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="36cd6-103">Api.JetRestoreInstance method</span></span>

<span data-ttu-id="36cd6-104">Ripristina e recupera un backup di flusso di un'istanza di, inclusi tutti i database collegati.</span><span class="sxs-lookup"><span data-stu-id="36cd6-104">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="36cd6-105">È progettato per funzionare con un backup creato con la funzione [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) .</span><span class="sxs-lookup"><span data-stu-id="36cd6-105">It is designed to work with a backup created with the [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) function.</span></span> <span data-ttu-id="36cd6-106">Si tratta della funzione di ripristino più semplice e incapsulata.</span><span class="sxs-lookup"><span data-stu-id="36cd6-106">This is the simplest and most encapsulated restore function.</span></span>

<span data-ttu-id="36cd6-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36cd6-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36cd6-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36cd6-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36cd6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36cd6-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="36cd6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="36cd6-110">Parameters</span></span>

  - <span data-ttu-id="36cd6-111">instance</span><span class="sxs-lookup"><span data-stu-id="36cd6-111">instance</span></span>  
    <span data-ttu-id="36cd6-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36cd6-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="36cd6-113">Istanza di da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="36cd6-113">The instance to use.</span></span> <span data-ttu-id="36cd6-114">L'istanza non deve essere inizializzata.</span><span class="sxs-lookup"><span data-stu-id="36cd6-114">The instance should not be initialized.</span></span> <span data-ttu-id="36cd6-115">Il ripristino dei file comporterà l'inizializzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="36cd6-115">Restoring the files will initialize the instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="36cd6-116">source</span><span class="sxs-lookup"><span data-stu-id="36cd6-116">source</span></span>  
    <span data-ttu-id="36cd6-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="36cd6-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="36cd6-118">Percorso del backup.</span><span class="sxs-lookup"><span data-stu-id="36cd6-118">Location of the backup.</span></span> <span data-ttu-id="36cd6-119">Il backup dovrebbe essere stato creato con [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="36cd6-119">The backup should have been created with [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="36cd6-120">destination</span><span class="sxs-lookup"><span data-stu-id="36cd6-120">destination</span></span>  
    <span data-ttu-id="36cd6-121">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="36cd6-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="36cd6-122">Nome della cartella in cui verranno copiati e ripristinati i file di database del set di backup.</span><span class="sxs-lookup"><span data-stu-id="36cd6-122">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="36cd6-123">Se è impostato su null, i file di database verranno copiati e ripristinati nel percorso originale.</span><span class="sxs-lookup"><span data-stu-id="36cd6-123">If this is set to null, the database files will be copied and recovered to their original location.</span></span>

<!-- end list -->

  - <span data-ttu-id="36cd6-124">statusCallback</span><span class="sxs-lookup"><span data-stu-id="36cd6-124">statusCallback</span></span>  
    <span data-ttu-id="36cd6-125">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="36cd6-125">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="36cd6-126">Callback facoltativo della notifica di stato.</span><span class="sxs-lookup"><span data-stu-id="36cd6-126">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="36cd6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36cd6-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36cd6-128">Riferimento</span><span class="sxs-lookup"><span data-stu-id="36cd6-128">Reference</span></span>

[<span data-ttu-id="36cd6-129">Classe API</span><span class="sxs-lookup"><span data-stu-id="36cd6-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="36cd6-130">Membri API</span><span class="sxs-lookup"><span data-stu-id="36cd6-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="36cd6-131">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="36cd6-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
