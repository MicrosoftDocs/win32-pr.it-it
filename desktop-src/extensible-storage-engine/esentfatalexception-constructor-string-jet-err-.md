---
description: 'Altre informazioni su: Costruttore EsentFatalException (String, JET_err)'
title: Costruttore EsentFatalException (String, JET_err)
TOCTitle: EsentFatalException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101610
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
ms.openlocfilehash: f025b93e626c4b0f2ab6bb7729169aaff1d67707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231653"
---
# <a name="esentfatalexception-constructor-string-jet_err"></a><span data-ttu-id="66bcf-103">Costruttore EsentFatalException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="66bcf-103">EsentFatalException constructor (String, JET_err)</span></span>

<span data-ttu-id="66bcf-104">Inizializza una nuova istanza della classe EsentFatalException.</span><span class="sxs-lookup"><span data-stu-id="66bcf-104">Initializes a new instance of the EsentFatalException class.</span></span>

<span data-ttu-id="66bcf-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66bcf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66bcf-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66bcf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66bcf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66bcf-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentFatalException(description, _
    err)
```

``` csharp
protected EsentFatalException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="66bcf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="66bcf-108">Parameters</span></span>

  - <span data-ttu-id="66bcf-109">description</span><span class="sxs-lookup"><span data-stu-id="66bcf-109">description</span></span>  
    <span data-ttu-id="66bcf-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="66bcf-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="66bcf-111">Descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="66bcf-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="66bcf-112">Err</span><span class="sxs-lookup"><span data-stu-id="66bcf-112">err</span></span>  
    <span data-ttu-id="66bcf-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="66bcf-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="66bcf-114">Codice di errore dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="66bcf-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="66bcf-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66bcf-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66bcf-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="66bcf-116">Reference</span></span>

[<span data-ttu-id="66bcf-117">Classe EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="66bcf-117">EsentFatalException class</span></span>](./esentfatalexception-class.md)

[<span data-ttu-id="66bcf-118">Membri di EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="66bcf-118">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="66bcf-119">Overload EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="66bcf-119">EsentFatalException overload</span></span>](./esentfatalexception-constructor.md)

[<span data-ttu-id="66bcf-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="66bcf-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
