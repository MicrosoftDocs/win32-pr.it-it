---
description: 'Altre informazioni su: classe EsentIOException'
title: Classe EsentIOException
TOCTitle: EsentIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fbcbf38ae60ae17f74e650c403611a88d89662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319744"
---
# <a name="esentioexception-class"></a><span data-ttu-id="701b9-103">Classe EsentIOException</span><span class="sxs-lookup"><span data-stu-id="701b9-103">EsentIOException class</span></span>

<span data-ttu-id="701b9-104">Classe di base per le eccezioni IO.</span><span class="sxs-lookup"><span data-stu-id="701b9-104">Base class for IO exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="701b9-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="701b9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="701b9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="701b9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="701b9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="701b9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="701b9-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="701b9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="701b9-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="701b9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="701b9-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="701b9-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="701b9-111">Microsoft. ISAM. esent. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="701b9-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>  
            [<span data-ttu-id="701b9-112">Microsoft. ISAM. esent. Interop. EsentDeleteBackupFileFailException</span><span class="sxs-lookup"><span data-stu-id="701b9-112">Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException</span></span>](./esentdeletebackupfilefailexception-class.md)  
            [<span data-ttu-id="701b9-113">Microsoft. ISAM. esent. Interop. EsentDiskIOException</span><span class="sxs-lookup"><span data-stu-id="701b9-113">Microsoft.Isam.Esent.Interop.EsentDiskIOException</span></span>](./esentdiskioexception-class.md)  
            [<span data-ttu-id="701b9-114">Microsoft. ISAM. esent. Interop. EsentFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="701b9-114">Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException</span></span>](./esentfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="701b9-115">Microsoft. ISAM. esent. Interop. EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="701b9-115">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>](./esentlogwritefailexception-class.md)  
            [<span data-ttu-id="701b9-116">Microsoft. ISAM. esent. Interop. EsentMakeBackupDirectoryFailException</span><span class="sxs-lookup"><span data-stu-id="701b9-116">Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException</span></span>](./esentmakebackupdirectoryfailexception-class.md)  

<span data-ttu-id="701b9-117">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="701b9-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="701b9-118">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="701b9-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="701b9-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="701b9-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentIOException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentIOException
```

``` csharp
[SerializableAttribute]
public abstract class EsentIOException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="701b9-120">Thread safety</span><span class="sxs-lookup"><span data-stu-id="701b9-120">Thread safety</span></span>

<span data-ttu-id="701b9-121">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="701b9-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="701b9-122">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="701b9-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="701b9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="701b9-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="701b9-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="701b9-124">Reference</span></span>

[<span data-ttu-id="701b9-125">Membri di EsentIOException</span><span class="sxs-lookup"><span data-stu-id="701b9-125">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="701b9-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="701b9-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
