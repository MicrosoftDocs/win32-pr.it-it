---
description: 'Altre informazioni su: Costruttore EsentStateException (String, JET_err)'
title: Costruttore EsentStateException (String, JET_err)
TOCTitle: EsentStateException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102995
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611671bb488d4804fd31569f15ab89e3ddfed462
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317432"
---
# <a name="esentstateexception-constructor-string-jet_err"></a><span data-ttu-id="6e72a-103">Costruttore EsentStateException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="6e72a-103">EsentStateException constructor (String, JET_err)</span></span>

<span data-ttu-id="6e72a-104">Inizializza una nuova istanza della classe EsentStateException.</span><span class="sxs-lookup"><span data-stu-id="6e72a-104">Initializes a new instance of the EsentStateException class.</span></span>

<span data-ttu-id="6e72a-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e72a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e72a-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e72a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e72a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e72a-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentStateException(description, _
    err)
```

``` csharp
protected EsentStateException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="6e72a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e72a-108">Parameters</span></span>

  - <span data-ttu-id="6e72a-109">description</span><span class="sxs-lookup"><span data-stu-id="6e72a-109">description</span></span>  
    <span data-ttu-id="6e72a-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6e72a-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6e72a-111">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="6e72a-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e72a-112">Err</span><span class="sxs-lookup"><span data-stu-id="6e72a-112">err</span></span>  
    <span data-ttu-id="6e72a-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6e72a-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="6e72a-114">Codice di errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="6e72a-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e72a-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e72a-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e72a-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6e72a-116">Reference</span></span>

[<span data-ttu-id="6e72a-117">Classe EsentStateException</span><span class="sxs-lookup"><span data-stu-id="6e72a-117">EsentStateException class</span></span>](./esentstateexception-class.md)

[<span data-ttu-id="6e72a-118">Membri di EsentStateException</span><span class="sxs-lookup"><span data-stu-id="6e72a-118">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="6e72a-119">Overload EsentStateException</span><span class="sxs-lookup"><span data-stu-id="6e72a-119">EsentStateException overload</span></span>](./esentstateexception-constructor.md)

[<span data-ttu-id="6e72a-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6e72a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
