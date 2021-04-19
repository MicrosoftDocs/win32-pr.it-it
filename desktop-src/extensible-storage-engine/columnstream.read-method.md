---
description: 'Altre informazioni su: ColumnStream. Read (metodo)'
title: Metodo ColumnStream. Read
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317516"
---
# <a name="columnstreamread-method"></a><span data-ttu-id="53621-103">Metodo ColumnStream. Read</span><span class="sxs-lookup"><span data-stu-id="53621-103">ColumnStream.Read method</span></span>

<span data-ttu-id="53621-104">Legge una sequenza di byte dal flusso corrente e fa avanzare la posizione nel flusso del numero di byte letti.</span><span class="sxs-lookup"><span data-stu-id="53621-104">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span>

<span data-ttu-id="53621-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53621-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53621-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53621-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53621-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53621-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="53621-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53621-108">Parameters</span></span>

  - <span data-ttu-id="53621-109">buffer</span><span class="sxs-lookup"><span data-stu-id="53621-109">buffer</span></span>  
    <span data-ttu-id="53621-110">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="53621-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="53621-111">Buffer in cui leggere.</span><span class="sxs-lookup"><span data-stu-id="53621-111">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="53621-112">offset</span><span class="sxs-lookup"><span data-stu-id="53621-112">offset</span></span>  
    <span data-ttu-id="53621-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53621-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="53621-114">Offset nel buffer in cui leggere.</span><span class="sxs-lookup"><span data-stu-id="53621-114">The offset in the buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="53621-115">count</span><span class="sxs-lookup"><span data-stu-id="53621-115">count</span></span>  
    <span data-ttu-id="53621-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53621-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="53621-117">Numero di byte da leggere.</span><span class="sxs-lookup"><span data-stu-id="53621-117">The number of bytes to read.</span></span>

#### <a name="return-value"></a><span data-ttu-id="53621-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53621-118">Return value</span></span>

<span data-ttu-id="53621-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53621-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="53621-120">Numero di byte letti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="53621-120">The number of bytes read into the buffer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="53621-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53621-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53621-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="53621-122">Reference</span></span>

[<span data-ttu-id="53621-123">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="53621-123">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="53621-124">Membri di ColumnStream</span><span class="sxs-lookup"><span data-stu-id="53621-124">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="53621-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53621-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
