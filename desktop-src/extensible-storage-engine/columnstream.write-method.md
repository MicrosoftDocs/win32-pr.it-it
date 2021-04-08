---
description: 'Altre informazioni su: ColumnStream. Write (metodo)'
title: Metodo ColumnStream. Write
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058172"
---
# <a name="columnstreamwrite-method"></a><span data-ttu-id="08c5d-103">Metodo ColumnStream. Write</span><span class="sxs-lookup"><span data-stu-id="08c5d-103">ColumnStream.Write method</span></span>

<span data-ttu-id="08c5d-104">Scrive una sequenza di byte nel flusso corrente e fa avanzare la posizione corrente nel flusso del numero di byte scritti.</span><span class="sxs-lookup"><span data-stu-id="08c5d-104">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span>

<span data-ttu-id="08c5d-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08c5d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08c5d-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08c5d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08c5d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08c5d-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="08c5d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="08c5d-108">Parameters</span></span>

  - <span data-ttu-id="08c5d-109">buffer</span><span class="sxs-lookup"><span data-stu-id="08c5d-109">buffer</span></span>  
    <span data-ttu-id="08c5d-110">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="08c5d-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="08c5d-111">Buffer da cui scrivere.</span><span class="sxs-lookup"><span data-stu-id="08c5d-111">The buffer to write from.</span></span>

<!-- end list -->

  - <span data-ttu-id="08c5d-112">offset</span><span class="sxs-lookup"><span data-stu-id="08c5d-112">offset</span></span>  
    <span data-ttu-id="08c5d-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="08c5d-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="08c5d-114">Offset nel buffer da scrivere.</span><span class="sxs-lookup"><span data-stu-id="08c5d-114">The offset in the buffer to write.</span></span>

<!-- end list -->

  - <span data-ttu-id="08c5d-115">count</span><span class="sxs-lookup"><span data-stu-id="08c5d-115">count</span></span>  
    <span data-ttu-id="08c5d-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="08c5d-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="08c5d-117">Numero di byte da scrivere.</span><span class="sxs-lookup"><span data-stu-id="08c5d-117">The number of bytes to write.</span></span>

## <a name="see-also"></a><span data-ttu-id="08c5d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08c5d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08c5d-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="08c5d-119">Reference</span></span>

[<span data-ttu-id="08c5d-120">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="08c5d-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="08c5d-121">Membri di ColumnStream</span><span class="sxs-lookup"><span data-stu-id="08c5d-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="08c5d-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="08c5d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
