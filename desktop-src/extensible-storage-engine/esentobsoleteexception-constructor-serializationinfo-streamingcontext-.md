---
description: 'Altre informazioni su: Costruttore EsentObsoleteException (SerializationInfo, StreamingContext)'
title: Costruttore EsentObsoleteException (SerializationInfo, StreamingContext)
TOCTitle: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102167
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b287a61396f0d908c888b84553e5dc67df907be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310896"
---
# <a name="esentobsoleteexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="ed63e-103">Costruttore EsentObsoleteException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="ed63e-103">EsentObsoleteException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="ed63e-104">Inizializza una nuova istanza della classe EsentObsoleteException.</span><span class="sxs-lookup"><span data-stu-id="ed63e-104">Initializes a new instance of the EsentObsoleteException class.</span></span> <span data-ttu-id="ed63e-105">Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.</span><span class="sxs-lookup"><span data-stu-id="ed63e-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="ed63e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed63e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed63e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed63e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed63e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed63e-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentObsoleteException(info, context)
```

``` csharp
protected EsentObsoleteException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="ed63e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed63e-109">Parameters</span></span>

  - <span data-ttu-id="ed63e-110">info</span><span class="sxs-lookup"><span data-stu-id="ed63e-110">info</span></span>  
    <span data-ttu-id="ed63e-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="ed63e-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="ed63e-112">Dati necessari per deserializzare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ed63e-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed63e-113">contesto</span><span class="sxs-lookup"><span data-stu-id="ed63e-113">context</span></span>  
    <span data-ttu-id="ed63e-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="ed63e-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="ed63e-115">Contesto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="ed63e-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed63e-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed63e-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed63e-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ed63e-117">Reference</span></span>

[<span data-ttu-id="ed63e-118">Classe EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="ed63e-118">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="ed63e-119">Membri di EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="ed63e-119">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="ed63e-120">Overload EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="ed63e-120">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="ed63e-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ed63e-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
