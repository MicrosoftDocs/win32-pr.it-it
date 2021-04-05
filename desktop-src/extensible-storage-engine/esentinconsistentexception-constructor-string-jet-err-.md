---
description: 'Altre informazioni su: Costruttore EsentInconsistentException (String, JET_err)'
title: Costruttore EsentInconsistentException (String, JET_err)
TOCTitle: EsentInconsistentException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInconsistentException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101740
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96d8b7a055d07ae120a23665004712772f67f215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752642"
---
# <a name="esentinconsistentexception-constructor-string-jet_err"></a><span data-ttu-id="0ee31-103">Costruttore EsentInconsistentException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="0ee31-103">EsentInconsistentException constructor (String, JET_err)</span></span>

<span data-ttu-id="0ee31-104">Inizializza una nuova istanza della classe EsentInconsistentException.</span><span class="sxs-lookup"><span data-stu-id="0ee31-104">Initializes a new instance of the EsentInconsistentException class.</span></span>

<span data-ttu-id="0ee31-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0ee31-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0ee31-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0ee31-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee31-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ee31-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentInconsistentException(description, _
    err)
```

``` csharp
protected EsentInconsistentException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="0ee31-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ee31-108">Parameters</span></span>

  - <span data-ttu-id="0ee31-109">description</span><span class="sxs-lookup"><span data-stu-id="0ee31-109">description</span></span>  
    <span data-ttu-id="0ee31-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0ee31-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0ee31-111">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="0ee31-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="0ee31-112">Err</span><span class="sxs-lookup"><span data-stu-id="0ee31-112">err</span></span>  
    <span data-ttu-id="0ee31-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0ee31-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="0ee31-114">Codice di errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="0ee31-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ee31-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ee31-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ee31-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0ee31-116">Reference</span></span>

[<span data-ttu-id="0ee31-117">Classe EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="0ee31-117">EsentInconsistentException class</span></span>](./esentinconsistentexception-class.md)

[<span data-ttu-id="0ee31-118">Membri di EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="0ee31-118">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="0ee31-119">Overload EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="0ee31-119">EsentInconsistentException overload</span></span>](./esentinconsistentexception-constructor.md)

[<span data-ttu-id="0ee31-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0ee31-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
