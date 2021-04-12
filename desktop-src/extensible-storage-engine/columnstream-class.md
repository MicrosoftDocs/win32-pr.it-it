---
description: 'Altre informazioni su: classe ColumnStream'
title: Classe ColumnStream
TOCTitle: ColumnStream class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eea249347acd18ec71f03fcdc82b8a2baa1da9ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232198"
---
# <a name="columnstream-class"></a><span data-ttu-id="f8266-103">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="f8266-103">ColumnStream class</span></span>

<span data-ttu-id="f8266-104">Questa classe fornisce un'interfaccia di flusso a una colonna con valore Long, ovvero una colonna di tipo [LongBinary](./jet-coltyp-enumeration.md) o [LONGTEXT](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f8266-104">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f8266-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="f8266-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f8266-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f8266-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f8266-107">System.MarshalByRefObject</span><span class="sxs-lookup"><span data-stu-id="f8266-107">System.MarshalByRefObject</span></span>](/dotnet/api/system.marshalbyrefobject)  
    [<span data-ttu-id="f8266-108">System. IO. Stream</span><span class="sxs-lookup"><span data-stu-id="f8266-108">System.IO.Stream</span></span>](/dotnet/api/system.io.stream)  
      <span data-ttu-id="f8266-109">Microsoft. ISAM. esent. Interop. ColumnStream</span><span class="sxs-lookup"><span data-stu-id="f8266-109">Microsoft.Isam.Esent.Interop.ColumnStream</span></span>  

<span data-ttu-id="f8266-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8266-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8266-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8266-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8266-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8266-112">Syntax</span></span>

``` vb
'Declaration
Public Class ColumnStream _
    Inherits Stream
'Usage
Dim instance As ColumnStream
```

``` csharp
public class ColumnStream : Stream
```

## <a name="thread-safety"></a><span data-ttu-id="f8266-113">Thread safety</span><span class="sxs-lookup"><span data-stu-id="f8266-113">Thread safety</span></span>

<span data-ttu-id="f8266-114">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f8266-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f8266-115">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f8266-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8266-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8266-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8266-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f8266-117">Reference</span></span>

[<span data-ttu-id="f8266-118">Membri di ColumnStream</span><span class="sxs-lookup"><span data-stu-id="f8266-118">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="f8266-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f8266-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
