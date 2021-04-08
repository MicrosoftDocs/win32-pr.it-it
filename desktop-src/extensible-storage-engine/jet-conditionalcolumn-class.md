---
description: 'Altre informazioni su: JET_CONDITIONALCOLUMN Class'
title: Classe JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn(v=EXCHG.10)
ms:contentKeyID: 55107506
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23b116ce88b24702711d74f610c208a72c44addf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967959"
---
# <a name="jet_conditionalcolumn-class"></a><span data-ttu-id="a7a30-103">Classe JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="a7a30-103">JET_CONDITIONALCOLUMN class</span></span>

<span data-ttu-id="a7a30-104">Definisce la modalità di esecuzione dell'indicizzazione condizionale per un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="a7a30-104">Defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="a7a30-105">Un indice condizionale contiene una voce di indice solo per le righe che corrispondono alla condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a7a30-105">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="a7a30-106">Tuttavia, la colonna condizionale non fa parte della chiave dell'indice, ma controlla solo la presenza della voce di indice.</span><span class="sxs-lookup"><span data-stu-id="a7a30-106">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a7a30-107">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a7a30-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="a7a30-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="a7a30-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="a7a30-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="a7a30-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span></span>  

<span data-ttu-id="a7a30-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7a30-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a7a30-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7a30-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7a30-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7a30-112">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_CONDITIONALCOLUMN _
    Implements IContentEquatable(Of JET_CONDITIONALCOLUMN), IDeepCloneable(Of JET_CONDITIONALCOLUMN)
'Usage
Dim instance As JET_CONDITIONALCOLUMN
```

``` csharp
[SerializableAttribute]
public sealed class JET_CONDITIONALCOLUMN : IContentEquatable<JET_CONDITIONALCOLUMN>, 
    IDeepCloneable<JET_CONDITIONALCOLUMN>
```

## <a name="thread-safety"></a><span data-ttu-id="a7a30-113">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a7a30-113">Thread safety</span></span>

<span data-ttu-id="a7a30-114">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a7a30-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a7a30-115">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a7a30-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7a30-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7a30-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7a30-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a7a30-117">Reference</span></span>

[<span data-ttu-id="a7a30-118">Membri JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="a7a30-118">JET_CONDITIONALCOLUMN members</span></span>](./jet-conditionalcolumn-members.md)

[<span data-ttu-id="a7a30-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a7a30-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
