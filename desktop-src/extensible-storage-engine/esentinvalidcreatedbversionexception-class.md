---
description: 'Altre informazioni su: classe EsentInvalidCreateDbVersionException'
title: Classe EsentInvalidCreateDbVersionException
TOCTitle: EsentInvalidCreateDbVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcreatedbversionexception(v=EXCHG.10)
ms:contentKeyID: 55101905
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 273b00900fece4afbb1329e25a36e50074e031dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880361"
---
# <a name="esentinvalidcreatedbversionexception-class"></a><span data-ttu-id="efc71-103">Classe EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="efc71-103">EsentInvalidCreateDbVersionException class</span></span>

<span data-ttu-id="efc71-104">Classe di base per JET_err. Eccezioni InvalidCreateDbVersion.</span><span class="sxs-lookup"><span data-stu-id="efc71-104">Base class for JET_err.InvalidCreateDbVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="efc71-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="efc71-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="efc71-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="efc71-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="efc71-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="efc71-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="efc71-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="efc71-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="efc71-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="efc71-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="efc71-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="efc71-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="efc71-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="efc71-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="efc71-112">Microsoft. ISAM. esent. Interop. EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="efc71-112">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>  

<span data-ttu-id="efc71-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="efc71-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="efc71-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="efc71-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="efc71-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efc71-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidCreateDbVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidCreateDbVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidCreateDbVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="efc71-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="efc71-116">Thread safety</span></span>

<span data-ttu-id="efc71-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="efc71-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="efc71-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="efc71-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="efc71-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efc71-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="efc71-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="efc71-120">Reference</span></span>

[<span data-ttu-id="efc71-121">Membri di EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="efc71-121">EsentInvalidCreateDbVersionException members</span></span>](./esentinvalidcreatedbversionexception-members.md)

[<span data-ttu-id="efc71-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="efc71-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
