---
description: 'Altre informazioni su: Costruttore EsentFatalException (SerializationInfo, StreamingContext)'
title: Costruttore EsentFatalException (SerializationInfo, StreamingContext)
TOCTitle: EsentFatalException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101554
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2264e3852eb6809f321b9bae162a833e86d7b513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049581"
---
# <a name="esentfatalexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="085bb-103">Costruttore EsentFatalException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="085bb-103">EsentFatalException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="085bb-104">Inizializza una nuova istanza della classe EsentFatalException.</span><span class="sxs-lookup"><span data-stu-id="085bb-104">Initializes a new instance of the EsentFatalException class.</span></span> <span data-ttu-id="085bb-105">Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.</span><span class="sxs-lookup"><span data-stu-id="085bb-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="085bb-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="085bb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="085bb-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="085bb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="085bb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="085bb-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFatalException(info, context)
```

``` csharp
protected EsentFatalException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="085bb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="085bb-109">Parameters</span></span>

  - <span data-ttu-id="085bb-110">info</span><span class="sxs-lookup"><span data-stu-id="085bb-110">info</span></span>  
    <span data-ttu-id="085bb-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="085bb-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="085bb-112">Dati necessari per deserializzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="085bb-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="085bb-113">contesto</span><span class="sxs-lookup"><span data-stu-id="085bb-113">context</span></span>  
    <span data-ttu-id="085bb-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="085bb-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="085bb-115">Contesto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="085bb-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="085bb-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="085bb-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="085bb-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="085bb-117">Reference</span></span>

[<span data-ttu-id="085bb-118">Classe EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="085bb-118">EsentFatalException class</span></span>](./esentfatalexception-class.md)

[<span data-ttu-id="085bb-119">Membri di EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="085bb-119">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="085bb-120">Overload EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="085bb-120">EsentFatalException overload</span></span>](./esentfatalexception-constructor.md)

[<span data-ttu-id="085bb-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="085bb-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
