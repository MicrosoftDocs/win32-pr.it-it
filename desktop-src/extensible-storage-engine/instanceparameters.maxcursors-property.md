---
description: 'Altre informazioni su: Proprietà InstanceParameters. MaxCursors'
title: Proprietà InstanceParameters. MaxCursors
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 029ff7c41916e668f532be60f018870f30e487ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319694"
---
# <a name="instanceparametersmaxcursors-property"></a><span data-ttu-id="755ef-103">Proprietà InstanceParameters. MaxCursors</span><span class="sxs-lookup"><span data-stu-id="755ef-103">InstanceParameters.MaxCursors property</span></span>

<span data-ttu-id="755ef-104">Ottiene o imposta il numero di risorse del cursore riservate per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="755ef-104">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="755ef-105">Una risorsa di cursore corrisponde direttamente a una JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="755ef-105">A cursor resource directly corresponds to a JET_TABLEID.</span></span>

<span data-ttu-id="755ef-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="755ef-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="755ef-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="755ef-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="755ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="755ef-108">Syntax</span></span>

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="755ef-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="755ef-109">Property value</span></span>

<span data-ttu-id="755ef-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="755ef-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="755ef-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="755ef-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="755ef-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="755ef-112">Reference</span></span>

[<span data-ttu-id="755ef-113">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="755ef-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="755ef-114">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="755ef-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="755ef-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="755ef-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
