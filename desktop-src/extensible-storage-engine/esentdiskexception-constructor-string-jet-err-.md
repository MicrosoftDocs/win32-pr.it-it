---
description: 'Altre informazioni su: Costruttore EsentDiskException (String, JET_err)'
title: Costruttore EsentDiskException (String, JET_err)
TOCTitle: EsentDiskException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101616
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d518fcb263481c2563b92d0b579a686db13c0175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318776"
---
# <a name="esentdiskexception-constructor-string-jet_err"></a><span data-ttu-id="358c7-103">Costruttore EsentDiskException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="358c7-103">EsentDiskException constructor (String, JET_err)</span></span>

<span data-ttu-id="358c7-104">Inizializza una nuova istanza della classe EsentDiskException.</span><span class="sxs-lookup"><span data-stu-id="358c7-104">Initializes a new instance of the EsentDiskException class.</span></span>

<span data-ttu-id="358c7-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="358c7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="358c7-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="358c7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="358c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="358c7-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentDiskException(description, _
    err)
```

``` csharp
protected EsentDiskException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="358c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="358c7-108">Parameters</span></span>

  - <span data-ttu-id="358c7-109">description</span><span class="sxs-lookup"><span data-stu-id="358c7-109">description</span></span>  
    <span data-ttu-id="358c7-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="358c7-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="358c7-111">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="358c7-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="358c7-112">Err</span><span class="sxs-lookup"><span data-stu-id="358c7-112">err</span></span>  
    <span data-ttu-id="358c7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="358c7-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="358c7-114">Codice di errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="358c7-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="358c7-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="358c7-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="358c7-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="358c7-116">Reference</span></span>

[<span data-ttu-id="358c7-117">Classe EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="358c7-117">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="358c7-118">Membri di EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="358c7-118">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="358c7-119">Overload EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="358c7-119">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="358c7-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="358c7-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
