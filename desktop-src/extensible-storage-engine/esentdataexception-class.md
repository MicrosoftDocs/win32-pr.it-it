---
description: 'Altre informazioni su: classe EsentDataException'
title: Classe EsentDataException
TOCTitle: EsentDataException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDataException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDataException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 996839740d1b008ffae12cf823b9664bf8ca4273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309710"
---
# <a name="esentdataexception-class"></a><span data-ttu-id="c832a-103">Classe EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c832a-103">EsentDataException class</span></span>

<span data-ttu-id="c832a-104">Classe di base per le eccezioni dei dati.</span><span class="sxs-lookup"><span data-stu-id="c832a-104">Base class for Data exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c832a-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="c832a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c832a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c832a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c832a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c832a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c832a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c832a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c832a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c832a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="c832a-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c832a-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>  
          [<span data-ttu-id="c832a-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="c832a-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
          [<span data-ttu-id="c832a-112">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="c832a-112">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
          [<span data-ttu-id="c832a-113">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="c832a-113">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  

<span data-ttu-id="c832a-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c832a-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c832a-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c832a-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c832a-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c832a-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDataException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentDataException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDataException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="c832a-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="c832a-117">Thread safety</span></span>

<span data-ttu-id="c832a-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c832a-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c832a-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c832a-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c832a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c832a-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c832a-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c832a-121">Reference</span></span>

[<span data-ttu-id="c832a-122">Membri di EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c832a-122">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="c832a-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c832a-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
