---
description: 'Altre informazioni su: metodo API. JetBackupInstance'
title: API. JetBackupInstance, metodo
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128058"
---
# <a name="apijetbackupinstance-method"></a><span data-ttu-id="679e1-103">API. JetBackupInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="679e1-103">Api.JetBackupInstance method</span></span>

<span data-ttu-id="679e1-104">Esegue un backup di flusso di un'istanza, inclusi tutti i database collegati, in una directory.</span><span class="sxs-lookup"><span data-stu-id="679e1-104">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="679e1-105">Con più metodi di backup supportati dal motore di, questa è la funzione più semplice e incapsulata.</span><span class="sxs-lookup"><span data-stu-id="679e1-105">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="679e1-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="679e1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="679e1-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="679e1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="679e1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="679e1-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="679e1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="679e1-109">Parameters</span></span>

  - <span data-ttu-id="679e1-110">instance</span><span class="sxs-lookup"><span data-stu-id="679e1-110">instance</span></span>  
    <span data-ttu-id="679e1-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="679e1-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="679e1-112">Istanza di di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="679e1-112">The instance to backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="679e1-113">destination</span><span class="sxs-lookup"><span data-stu-id="679e1-113">destination</span></span>  
    <span data-ttu-id="679e1-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="679e1-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="679e1-115">Directory in cui deve essere archiviato il backup.</span><span class="sxs-lookup"><span data-stu-id="679e1-115">The directory where the backup is to be stored.</span></span> <span data-ttu-id="679e1-116">Se il percorso di backup è null per usare la funzione, i log vengono troncati, se possibile.</span><span class="sxs-lookup"><span data-stu-id="679e1-116">If the backup path is null to use the function will truncate the logs, if possible.</span></span>

<!-- end list -->

  - <span data-ttu-id="679e1-117">grbit</span><span class="sxs-lookup"><span data-stu-id="679e1-117">grbit</span></span>  
    <span data-ttu-id="679e1-118">Tipo: [Microsoft. ISAM. esent. Interop. BackupGrbit](./backupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="679e1-118">Type: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="679e1-119">Opzioni di backup.</span><span class="sxs-lookup"><span data-stu-id="679e1-119">Backup options.</span></span>

<!-- end list -->

  - <span data-ttu-id="679e1-120">statusCallback</span><span class="sxs-lookup"><span data-stu-id="679e1-120">statusCallback</span></span>  
    <span data-ttu-id="679e1-121">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="679e1-121">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="679e1-122">Callback facoltativo della notifica di stato.</span><span class="sxs-lookup"><span data-stu-id="679e1-122">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="679e1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="679e1-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="679e1-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="679e1-124">Reference</span></span>

[<span data-ttu-id="679e1-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="679e1-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="679e1-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="679e1-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="679e1-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="679e1-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
