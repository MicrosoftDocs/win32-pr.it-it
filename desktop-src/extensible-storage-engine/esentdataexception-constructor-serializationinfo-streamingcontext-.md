---
description: 'Altre informazioni su: Costruttore EsentDataException (SerializationInfo, StreamingContext)'
title: Costruttore EsentDataException (SerializationInfo, StreamingContext)
TOCTitle: EsentDataException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101275
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43e7578adb10f607ff88062b48d3f2ebb73d34ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226776"
---
# <a name="esentdataexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="0d8d3-103">Costruttore EsentDataException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-103">EsentDataException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="0d8d3-104">Inizializza una nuova istanza della classe EsentDataException.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-104">Initializes a new instance of the EsentDataException class.</span></span> <span data-ttu-id="0d8d3-105">Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="0d8d3-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0d8d3-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8d3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d8d3-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDataException(info, context)
```

``` csharp
protected EsentDataException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="0d8d3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d8d3-109">Parameters</span></span>

  - <span data-ttu-id="0d8d3-110">info</span><span class="sxs-lookup"><span data-stu-id="0d8d3-110">info</span></span>  
    <span data-ttu-id="0d8d3-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="0d8d3-112">Dati necessari per deserializzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d8d3-113">contesto</span><span class="sxs-lookup"><span data-stu-id="0d8d3-113">context</span></span>  
    <span data-ttu-id="0d8d3-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="0d8d3-115">Contesto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d8d3-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d8d3-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d8d3-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0d8d3-117">Reference</span></span>

[<span data-ttu-id="0d8d3-118">Classe EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0d8d3-118">EsentDataException class</span></span>](./esentdataexception-class.md)

[<span data-ttu-id="0d8d3-119">Membri di EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0d8d3-119">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="0d8d3-120">Overload EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0d8d3-120">EsentDataException overload</span></span>](./esentdataexception-constructor.md)

[<span data-ttu-id="0d8d3-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0d8d3-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
