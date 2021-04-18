---
description: 'Altre informazioni su: classe EsentUnicodeNormalizationNotSupportedException'
title: Classe EsentUnicodeNormalizationNotSupportedException
TOCTitle: EsentUnicodeNormalizationNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunicodenormalizationnotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f11b74602997f356bea15e6b0d422ab30e3775be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316510"
---
# <a name="esentunicodenormalizationnotsupportedexception-class"></a><span data-ttu-id="a3154-103">Classe EsentUnicodeNormalizationNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="a3154-103">EsentUnicodeNormalizationNotSupportedException class</span></span>

<span data-ttu-id="a3154-104">Classe di base per JET_err. Eccezioni UnicodeNormalizationNotSupported.</span><span class="sxs-lookup"><span data-stu-id="a3154-104">Base class for JET_err.UnicodeNormalizationNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a3154-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a3154-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a3154-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a3154-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a3154-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a3154-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a3154-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a3154-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a3154-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a3154-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a3154-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a3154-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a3154-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a3154-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a3154-112">Microsoft. ISAM. esent. Interop. EsentUnicodeNormalizationNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="a3154-112">Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException</span></span>  

<span data-ttu-id="a3154-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a3154-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a3154-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a3154-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a3154-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3154-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnicodeNormalizationNotSupportedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentUnicodeNormalizationNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnicodeNormalizationNotSupportedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a3154-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a3154-116">Thread safety</span></span>

<span data-ttu-id="a3154-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a3154-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a3154-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a3154-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3154-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3154-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a3154-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a3154-120">Reference</span></span>

[<span data-ttu-id="a3154-121">Membri di EsentUnicodeNormalizationNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="a3154-121">EsentUnicodeNormalizationNotSupportedException members</span></span>](./esentunicodenormalizationnotsupportedexception-members.md)

[<span data-ttu-id="a3154-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a3154-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
