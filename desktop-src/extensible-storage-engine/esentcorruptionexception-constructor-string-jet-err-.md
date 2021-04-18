---
description: 'Altre informazioni su: Costruttore EsentCorruptionException (String, JET_err)'
title: Costruttore EsentCorruptionException (String, JET_err)
TOCTitle: EsentCorruptionException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101380
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30ed98ea56fe791ed949edc82b548990371c9671
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525068"
---
# <a name="esentcorruptionexception-constructor-string-jet_err"></a><span data-ttu-id="5134b-103">Costruttore EsentCorruptionException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="5134b-103">EsentCorruptionException constructor (String, JET_err)</span></span>

<span data-ttu-id="5134b-104">Inizializza una nuova istanza della classe EsentCorruptionException.</span><span class="sxs-lookup"><span data-stu-id="5134b-104">Initializes a new instance of the EsentCorruptionException class.</span></span>

<span data-ttu-id="5134b-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5134b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5134b-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5134b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5134b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5134b-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentCorruptionException(description, _
    err)
```

``` csharp
protected EsentCorruptionException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="5134b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5134b-108">Parameters</span></span>

  - <span data-ttu-id="5134b-109">description</span><span class="sxs-lookup"><span data-stu-id="5134b-109">description</span></span>  
    <span data-ttu-id="5134b-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5134b-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5134b-111">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="5134b-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="5134b-112">Err</span><span class="sxs-lookup"><span data-stu-id="5134b-112">err</span></span>  
    <span data-ttu-id="5134b-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5134b-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="5134b-114">Codice di errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="5134b-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="5134b-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5134b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5134b-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5134b-116">Reference</span></span>

[<span data-ttu-id="5134b-117">Classe EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="5134b-117">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="5134b-118">Membri di EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="5134b-118">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="5134b-119">Overload EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="5134b-119">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="5134b-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5134b-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
