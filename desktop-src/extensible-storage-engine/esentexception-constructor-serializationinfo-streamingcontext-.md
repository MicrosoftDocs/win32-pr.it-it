---
description: 'Altre informazioni su: Costruttore EsentException (SerializationInfo, StreamingContext)'
title: Costruttore EsentException (SerializationInfo, StreamingContext) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bdcfe5c3b37746f50926850b45763f9d70de893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319777"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="8f34c-103">Costruttore EsentException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="8f34c-103">EsentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="8f34c-104">Inizializza una nuova istanza della classe EsentException.</span><span class="sxs-lookup"><span data-stu-id="8f34c-104">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="8f34c-105">Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.</span><span class="sxs-lookup"><span data-stu-id="8f34c-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="8f34c-106">**Spazio dei nomi:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8f34c-106">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="8f34c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8f34c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8f34c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f34c-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="8f34c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f34c-109">Parameters</span></span>

  - <span data-ttu-id="8f34c-110">info</span><span class="sxs-lookup"><span data-stu-id="8f34c-110">info</span></span>  
    <span data-ttu-id="8f34c-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="8f34c-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="8f34c-112">Dati necessari per deserializzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f34c-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="8f34c-113">contesto</span><span class="sxs-lookup"><span data-stu-id="8f34c-113">context</span></span>  
    <span data-ttu-id="8f34c-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="8f34c-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="8f34c-115">Contesto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="8f34c-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f34c-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f34c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8f34c-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8f34c-117">Reference</span></span>

[<span data-ttu-id="8f34c-118">Classe EsentException</span><span class="sxs-lookup"><span data-stu-id="8f34c-118">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="8f34c-119">Membri di EsentException</span><span class="sxs-lookup"><span data-stu-id="8f34c-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="8f34c-120">Overload EsentException</span><span class="sxs-lookup"><span data-stu-id="8f34c-120">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="8f34c-121">Spazio dei nomi Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="8f34c-121">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
