---
description: 'Altre informazioni su: Proprietà InstanceParameters. OneDatabasePerSession'
title: Proprietà InstanceParameters. OneDatabasePerSession
TOCTitle: 'OneDatabasePerSession property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.onedatabasepersession(v=EXCHG.10)
ms:contentKeyID: 55103319
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_OneDatabasePerSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c130a00b8fcbcbcf6a8fc7bbdbbad6a4e36f218e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319693"
---
# <a name="instanceparametersonedatabasepersession-property"></a><span data-ttu-id="89a4c-103">Proprietà InstanceParameters. OneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="89a4c-103">InstanceParameters.OneDatabasePerSession property</span></span>

<span data-ttu-id="89a4c-104">Ottiene o imposta un valore che indica se è consentito l'apertura di un solo database tramite JetOpenDatabase da una sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="89a4c-104">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="89a4c-105">Il database temporaneo è escluso da questa restrizione.</span><span class="sxs-lookup"><span data-stu-id="89a4c-105">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="89a4c-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89a4c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89a4c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89a4c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89a4c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89a4c-108">Syntax</span></span>

``` vb
'Declaration
Public Property OneDatabasePerSession As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.OneDatabasePerSession

instance.OneDatabasePerSession = value
```

``` csharp
public bool OneDatabasePerSession { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="89a4c-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="89a4c-109">Property value</span></span>

<span data-ttu-id="89a4c-110">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="89a4c-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="89a4c-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89a4c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89a4c-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="89a4c-112">Reference</span></span>

[<span data-ttu-id="89a4c-113">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="89a4c-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="89a4c-114">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="89a4c-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="89a4c-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89a4c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
