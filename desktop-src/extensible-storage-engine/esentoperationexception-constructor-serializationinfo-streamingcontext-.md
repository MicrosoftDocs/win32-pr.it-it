---
description: 'Altre informazioni su: Costruttore EsentOperationException (SerializationInfo, StreamingContext)'
title: Costruttore EsentOperationException (SerializationInfo, StreamingContext)
TOCTitle: EsentOperationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102312
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ee281a47ae8e24ff51ffe5c3d6a4ef4f4b1873e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227162"
---
# <a name="esentoperationexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="6444a-103">Costruttore EsentOperationException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="6444a-103">EsentOperationException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="6444a-104">Inizializza una nuova istanza della classe EsentOperationException.</span><span class="sxs-lookup"><span data-stu-id="6444a-104">Initializes a new instance of the EsentOperationException class.</span></span> <span data-ttu-id="6444a-105">Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.</span><span class="sxs-lookup"><span data-stu-id="6444a-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="6444a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6444a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6444a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6444a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6444a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6444a-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentOperationException(info, context)
```

``` csharp
protected EsentOperationException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="6444a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6444a-109">Parameters</span></span>

  - <span data-ttu-id="6444a-110">info</span><span class="sxs-lookup"><span data-stu-id="6444a-110">info</span></span>  
    <span data-ttu-id="6444a-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="6444a-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="6444a-112">Dati necessari per deserializzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6444a-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="6444a-113">contesto</span><span class="sxs-lookup"><span data-stu-id="6444a-113">context</span></span>  
    <span data-ttu-id="6444a-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="6444a-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="6444a-115">Contesto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="6444a-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="6444a-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6444a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6444a-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6444a-117">Reference</span></span>

[<span data-ttu-id="6444a-118">Classe EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="6444a-118">EsentOperationException class</span></span>](./esentoperationexception-class.md)

[<span data-ttu-id="6444a-119">Membri di EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="6444a-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="6444a-120">Overload EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="6444a-120">EsentOperationException overload</span></span>](./esentoperationexception-constructor.md)

[<span data-ttu-id="6444a-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6444a-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
