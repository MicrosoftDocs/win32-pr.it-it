---
description: 'Altre informazioni su: Proprietà InstanceParameters. PageTempDBMin'
title: Proprietà InstanceParameters. PageTempDBMin
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06825762485ad52743d585ce0fed86bd1739cd21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313558"
---
# <a name="instanceparameterspagetempdbmin-property"></a><span data-ttu-id="66ea9-103">Proprietà InstanceParameters. PageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="66ea9-103">InstanceParameters.PageTempDBMin property</span></span>

<span data-ttu-id="66ea9-104">Ottiene o imposta le dimensioni iniziali del database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="66ea9-104">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="66ea9-105">Le dimensioni sono le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="66ea9-105">The size is in database pages.</span></span> <span data-ttu-id="66ea9-106">Una dimensione pari a zero indica che devono essere utilizzate le dimensioni predefinite di un database normale.</span><span class="sxs-lookup"><span data-stu-id="66ea9-106">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="66ea9-107">È spesso consigliabile che le piccole applicazioni configurino il database temporaneo in modo che sia il più piccolo possibile.</span><span class="sxs-lookup"><span data-stu-id="66ea9-107">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="66ea9-108">L'impostazione di questo parametro su [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) consente di ottenere il database temporaneo più piccolo possibile.</span><span class="sxs-lookup"><span data-stu-id="66ea9-108">Setting this parameter to [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) will achieve the smallest temporary database possible.</span></span>

<span data-ttu-id="66ea9-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66ea9-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66ea9-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66ea9-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66ea9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66ea9-111">Syntax</span></span>

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="66ea9-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="66ea9-112">Property value</span></span>

<span data-ttu-id="66ea9-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="66ea9-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="66ea9-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66ea9-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66ea9-115">Riferimento</span><span class="sxs-lookup"><span data-stu-id="66ea9-115">Reference</span></span>

[<span data-ttu-id="66ea9-116">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="66ea9-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="66ea9-117">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="66ea9-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="66ea9-118">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="66ea9-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
