---
description: 'Altre informazioni su: Costruttore EsentIOException (String, JET_err)'
title: Costruttore EsentIOException (String, JET_err)
TOCTitle: EsentIOException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102030
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
ms.openlocfilehash: 087f22d7836ff41ac97b65c15be1b51dfac84a8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312637"
---
# <a name="esentioexception-constructor-string-jet_err"></a><span data-ttu-id="a591b-103">Costruttore EsentIOException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="a591b-103">EsentIOException constructor (String, JET_err)</span></span>

<span data-ttu-id="a591b-104">Inizializza una nuova istanza della classe EsentIOException.</span><span class="sxs-lookup"><span data-stu-id="a591b-104">Initializes a new instance of the EsentIOException class.</span></span>

<span data-ttu-id="a591b-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a591b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a591b-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a591b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a591b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a591b-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentIOException(description, _
    err)
```

``` csharp
protected EsentIOException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="a591b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a591b-108">Parameters</span></span>

  - <span data-ttu-id="a591b-109">description</span><span class="sxs-lookup"><span data-stu-id="a591b-109">description</span></span>  
    <span data-ttu-id="a591b-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a591b-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a591b-111">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="a591b-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="a591b-112">Err</span><span class="sxs-lookup"><span data-stu-id="a591b-112">err</span></span>  
    <span data-ttu-id="a591b-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a591b-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="a591b-114">Codice di errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a591b-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="a591b-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a591b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a591b-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a591b-116">Reference</span></span>

[<span data-ttu-id="a591b-117">Classe EsentIOException</span><span class="sxs-lookup"><span data-stu-id="a591b-117">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="a591b-118">Membri di EsentIOException</span><span class="sxs-lookup"><span data-stu-id="a591b-118">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="a591b-119">Overload EsentIOException</span><span class="sxs-lookup"><span data-stu-id="a591b-119">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="a591b-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a591b-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
