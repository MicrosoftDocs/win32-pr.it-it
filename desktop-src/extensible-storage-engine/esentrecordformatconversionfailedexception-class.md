---
description: 'Altre informazioni su: classe EsentRecordFormatConversionFailedException'
title: Classe EsentRecordFormatConversionFailedException
TOCTitle: EsentRecordFormatConversionFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordformatconversionfailedexception(v=EXCHG.10)
ms:contentKeyID: 55102564
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1895eb3e7068106cc73bedc967b0c113c5c109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319228"
---
# <a name="esentrecordformatconversionfailedexception-class"></a><span data-ttu-id="54700-103">Classe EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="54700-103">EsentRecordFormatConversionFailedException class</span></span>

<span data-ttu-id="54700-104">Classe di base per JET_err. Eccezioni RecordFormatConversionFailed.</span><span class="sxs-lookup"><span data-stu-id="54700-104">Base class for JET_err.RecordFormatConversionFailed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="54700-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="54700-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="54700-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="54700-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="54700-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="54700-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="54700-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="54700-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="54700-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="54700-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="54700-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="54700-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="54700-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="54700-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="54700-112">Microsoft. ISAM. esent. Interop. EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="54700-112">Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException</span></span>  

<span data-ttu-id="54700-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="54700-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="54700-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="54700-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54700-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54700-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordFormatConversionFailedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRecordFormatConversionFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordFormatConversionFailedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="54700-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="54700-116">Thread safety</span></span>

<span data-ttu-id="54700-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="54700-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="54700-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="54700-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="54700-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54700-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54700-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="54700-120">Reference</span></span>

[<span data-ttu-id="54700-121">Membri di EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="54700-121">EsentRecordFormatConversionFailedException members</span></span>](./esentrecordformatconversionfailedexception-members.md)

[<span data-ttu-id="54700-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="54700-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
