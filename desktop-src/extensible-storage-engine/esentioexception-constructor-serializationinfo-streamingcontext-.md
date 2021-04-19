---
description: 'Altre informazioni su: Costruttore EsentIOException (SerializationInfo, StreamingContext)'
title: Costruttore EsentIOException (SerializationInfo, StreamingContext)
TOCTitle: EsentIOException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102032
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29d6b0666f4a1b38441c4f9878575b9867ae10c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319743"
---
# <a name="esentioexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="0c532-103">Costruttore EsentIOException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="0c532-103">EsentIOException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="0c532-104">Inizializza una nuova istanza della classe EsentIOException.</span><span class="sxs-lookup"><span data-stu-id="0c532-104">Initializes a new instance of the EsentIOException class.</span></span> <span data-ttu-id="0c532-105">Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.</span><span class="sxs-lookup"><span data-stu-id="0c532-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="0c532-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c532-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c532-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c532-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c532-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c532-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentIOException(info, context)
```

``` csharp
protected EsentIOException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="0c532-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c532-109">Parameters</span></span>

  - <span data-ttu-id="0c532-110">info</span><span class="sxs-lookup"><span data-stu-id="0c532-110">info</span></span>  
    <span data-ttu-id="0c532-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="0c532-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="0c532-112">Dati necessari per deserializzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c532-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c532-113">contesto</span><span class="sxs-lookup"><span data-stu-id="0c532-113">context</span></span>  
    <span data-ttu-id="0c532-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="0c532-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="0c532-115">Contesto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="0c532-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c532-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c532-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c532-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0c532-117">Reference</span></span>

[<span data-ttu-id="0c532-118">Classe EsentIOException</span><span class="sxs-lookup"><span data-stu-id="0c532-118">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="0c532-119">Membri di EsentIOException</span><span class="sxs-lookup"><span data-stu-id="0c532-119">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="0c532-120">Overload EsentIOException</span><span class="sxs-lookup"><span data-stu-id="0c532-120">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="0c532-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0c532-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
