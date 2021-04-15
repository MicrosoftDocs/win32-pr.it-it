---
description: 'Altre informazioni su: Costruttore EsentApiException (SerializationInfo, StreamingContext)'
title: Costruttore EsentApiException (SerializationInfo, StreamingContext)
TOCTitle: EsentApiException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101059
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a00204c254378956521a1ae5fe02480dd879c832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485876"
---
# <a name="esentapiexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="26f8f-103">Costruttore EsentApiException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="26f8f-103">EsentApiException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="26f8f-104">Inizializza una nuova istanza della classe EsentApiException.</span><span class="sxs-lookup"><span data-stu-id="26f8f-104">Initializes a new instance of the EsentApiException class.</span></span> <span data-ttu-id="26f8f-105">Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.</span><span class="sxs-lookup"><span data-stu-id="26f8f-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="26f8f-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="26f8f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="26f8f-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="26f8f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="26f8f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26f8f-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentApiException(info, context)
```

``` csharp
protected EsentApiException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="26f8f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="26f8f-109">Parameters</span></span>

  - <span data-ttu-id="26f8f-110">info</span><span class="sxs-lookup"><span data-stu-id="26f8f-110">info</span></span>  
    <span data-ttu-id="26f8f-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="26f8f-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="26f8f-112">Dati necessari per deserializzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26f8f-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="26f8f-113">contesto</span><span class="sxs-lookup"><span data-stu-id="26f8f-113">context</span></span>  
    <span data-ttu-id="26f8f-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="26f8f-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="26f8f-115">Contesto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="26f8f-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="26f8f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26f8f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26f8f-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="26f8f-117">Reference</span></span>

[<span data-ttu-id="26f8f-118">Classe EsentApiException</span><span class="sxs-lookup"><span data-stu-id="26f8f-118">EsentApiException class</span></span>](./esentapiexception-class.md)

[<span data-ttu-id="26f8f-119">Membri di EsentApiException</span><span class="sxs-lookup"><span data-stu-id="26f8f-119">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="26f8f-120">Overload EsentApiException</span><span class="sxs-lookup"><span data-stu-id="26f8f-120">EsentApiException overload</span></span>](./esentapiexception-constructor.md)

[<span data-ttu-id="26f8f-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="26f8f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
