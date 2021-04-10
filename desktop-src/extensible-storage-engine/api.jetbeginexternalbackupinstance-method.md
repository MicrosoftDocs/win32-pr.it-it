---
description: 'Altre informazioni su: metodo API. JetBeginExternalBackupInstance'
title: API. JetBeginExternalBackupInstance, metodo
TOCTitle: 'JetBeginExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100659
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c42f5d1f62de0af7582247fb47d407f82981a42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966565"
---
# <a name="apijetbeginexternalbackupinstance-method"></a><span data-ttu-id="b8d63-103">API. JetBeginExternalBackupInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="b8d63-103">Api.JetBeginExternalBackupInstance method</span></span>

<span data-ttu-id="b8d63-104">Avvia un backup esterno mentre il motore e il database sono online e attivi.</span><span class="sxs-lookup"><span data-stu-id="b8d63-104">Initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="b8d63-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8d63-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8d63-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8d63-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d63-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8d63-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginExternalBackupInstance ( _
    instance As JET_INSTANCE, _
    grbit As BeginExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As BeginExternalBackupGrbitApi.JetBeginExternalBackupInstance(instance, _
    grbit)
```

``` csharp
public static void JetBeginExternalBackupInstance(
    JET_INSTANCE instance,
    BeginExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b8d63-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8d63-108">Parameters</span></span>

  - <span data-ttu-id="b8d63-109">instance</span><span class="sxs-lookup"><span data-stu-id="b8d63-109">instance</span></span>  
    <span data-ttu-id="b8d63-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8d63-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b8d63-111">L'istanza prepara per il backup.</span><span class="sxs-lookup"><span data-stu-id="b8d63-111">The instance prepare for backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8d63-112">grbit</span><span class="sxs-lookup"><span data-stu-id="b8d63-112">grbit</span></span>  
    <span data-ttu-id="b8d63-113">Tipo: [Microsoft. ISAM. esent. Interop. BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b8d63-113">Type: [Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b8d63-114">Opzioni di backup.</span><span class="sxs-lookup"><span data-stu-id="b8d63-114">Backup options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8d63-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8d63-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8d63-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b8d63-116">Reference</span></span>

[<span data-ttu-id="b8d63-117">Classe API</span><span class="sxs-lookup"><span data-stu-id="b8d63-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b8d63-118">Membri API</span><span class="sxs-lookup"><span data-stu-id="b8d63-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b8d63-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b8d63-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
