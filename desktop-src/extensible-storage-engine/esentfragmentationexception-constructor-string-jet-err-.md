---
description: 'Altre informazioni su: Costruttore EsentFragmentationException (String, JET_err)'
title: Costruttore EsentFragmentationException (String, JET_err)
TOCTitle: EsentFragmentationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101778
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3c6492ac4055b985194b3849090672d471390cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129883"
---
# <a name="esentfragmentationexception-constructor-string-jet_err"></a><span data-ttu-id="90907-103">Costruttore EsentFragmentationException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="90907-103">EsentFragmentationException constructor (String, JET_err)</span></span>

<span data-ttu-id="90907-104">Inizializza una nuova istanza della classe EsentFragmentationException.</span><span class="sxs-lookup"><span data-stu-id="90907-104">Initializes a new instance of the EsentFragmentationException class.</span></span>

<span data-ttu-id="90907-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90907-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="90907-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90907-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90907-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90907-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentFragmentationException(description, _
    err)
```

``` csharp
protected EsentFragmentationException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="90907-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="90907-108">Parameters</span></span>

  - <span data-ttu-id="90907-109">description</span><span class="sxs-lookup"><span data-stu-id="90907-109">description</span></span>  
    <span data-ttu-id="90907-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="90907-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="90907-111">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="90907-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="90907-112">Err</span><span class="sxs-lookup"><span data-stu-id="90907-112">err</span></span>  
    <span data-ttu-id="90907-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="90907-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="90907-114">Codice di errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="90907-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="90907-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90907-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90907-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="90907-116">Reference</span></span>

[<span data-ttu-id="90907-117">Classe EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="90907-117">EsentFragmentationException class</span></span>](./esentfragmentationexception-class.md)

[<span data-ttu-id="90907-118">Membri di EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="90907-118">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="90907-119">Overload EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="90907-119">EsentFragmentationException overload</span></span>](./esentfragmentationexception-constructor.md)

[<span data-ttu-id="90907-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="90907-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
