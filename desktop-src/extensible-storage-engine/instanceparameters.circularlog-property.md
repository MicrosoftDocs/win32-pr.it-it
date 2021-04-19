---
description: 'Altre informazioni su: Proprietà InstanceParameters. CircularLog'
title: Proprietà InstanceParameters. CircularLog
TOCTitle: 'CircularLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.circularlog(v=EXCHG.10)
ms:contentKeyID: 55103320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CircularLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f9a77aa0d0f60b49269dc939787b165a3f2f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319696"
---
# <a name="instanceparameterscircularlog-property"></a><span data-ttu-id="283a4-103">Proprietà InstanceParameters. CircularLog</span><span class="sxs-lookup"><span data-stu-id="283a4-103">InstanceParameters.CircularLog property</span></span>

<span data-ttu-id="283a4-104">Ottiene o imposta un valore che indica se la registrazione circolare è attiva.</span><span class="sxs-lookup"><span data-stu-id="283a4-104">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="283a4-105">Quando la registrazione circolare è disattivata, tutti i file di log delle transazioni generati vengono conservati su disco fino a quando non sono più necessari perché è stato eseguito un backup completo del database.</span><span class="sxs-lookup"><span data-stu-id="283a4-105">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="283a4-106">Quando la registrazione circolare è attiva, solo i file di log delle transazioni più piccoli rispetto al checkpoint corrente vengono conservati su disco.</span><span class="sxs-lookup"><span data-stu-id="283a4-106">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="283a4-107">Il vantaggio di questa modalità è che non è necessario che i backup ritirino i vecchi file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="283a4-107">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span>

<span data-ttu-id="283a4-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="283a4-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="283a4-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="283a4-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="283a4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="283a4-110">Syntax</span></span>

``` vb
'Declaration
Public Property CircularLog As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CircularLog

instance.CircularLog = value
```

``` csharp
public bool CircularLog { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="283a4-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="283a4-111">Property value</span></span>

<span data-ttu-id="283a4-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="283a4-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="283a4-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="283a4-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="283a4-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="283a4-114">Reference</span></span>

[<span data-ttu-id="283a4-115">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="283a4-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="283a4-116">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="283a4-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="283a4-117">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="283a4-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
