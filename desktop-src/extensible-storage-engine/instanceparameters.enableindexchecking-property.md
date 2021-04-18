---
description: 'Altre informazioni su: Proprietà InstanceParameters. EnableIndexChecking'
title: Proprietà InstanceParameters. EnableIndexChecking
TOCTitle: 'EnableIndexChecking property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enableindexchecking(v=EXCHG.10)
ms:contentKeyID: 55103567
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableIndexChecking
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a3090c1e5c1e42aca3758496b1367f3932e123c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316501"
---
# <a name="instanceparametersenableindexchecking-property"></a><span data-ttu-id="6de72-103">Proprietà InstanceParameters. EnableIndexChecking</span><span class="sxs-lookup"><span data-stu-id="6de72-103">InstanceParameters.EnableIndexChecking property</span></span>

<span data-ttu-id="6de72-104">Ottiene o imposta un valore che indica se [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) verificherà la presenza di indici compilati utilizzando una versione precedente della libreria NLS nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6de72-104">Gets or sets a value indicating whether [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will check for indexes that were build using an older version of the NLS library in the operating system.</span></span>

<span data-ttu-id="6de72-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6de72-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6de72-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6de72-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6de72-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6de72-107">Syntax</span></span>

``` vb
'Declaration
Public Property EnableIndexChecking As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableIndexChecking

instance.EnableIndexChecking = value
```

``` csharp
public bool EnableIndexChecking { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6de72-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6de72-108">Property value</span></span>

<span data-ttu-id="6de72-109">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6de72-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6de72-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6de72-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6de72-111">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6de72-111">Reference</span></span>

[<span data-ttu-id="6de72-112">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="6de72-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="6de72-113">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="6de72-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="6de72-114">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6de72-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
