---
description: 'Altre informazioni su: costruttore di istanza (String, String, TermGrbit)'
title: Costruttore di istanza (String, String, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753303"
---
# <a name="instance-constructor-string-string-termgrbit"></a><span data-ttu-id="ee344-103">Costruttore di istanza (String, String, TermGrbit)</span><span class="sxs-lookup"><span data-stu-id="ee344-103">Instance constructor (String, String, TermGrbit)</span></span>

<span data-ttu-id="ee344-104">Inizializza una nuova istanza della classe dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ee344-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="ee344-105">Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="ee344-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="ee344-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee344-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ee344-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ee344-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee344-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee344-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ee344-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee344-109">Parameters</span></span>

  - <span data-ttu-id="ee344-110">name</span><span class="sxs-lookup"><span data-stu-id="ee344-110">name</span></span>  
    <span data-ttu-id="ee344-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ee344-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ee344-112">Nome dell’istanza.</span><span class="sxs-lookup"><span data-stu-id="ee344-112">The name of the instance.</span></span> <span data-ttu-id="ee344-113">Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.</span><span class="sxs-lookup"><span data-stu-id="ee344-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee344-114">displayName</span><span class="sxs-lookup"><span data-stu-id="ee344-114">displayName</span></span>  
    <span data-ttu-id="ee344-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ee344-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ee344-116">Nome visualizzato per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ee344-116">A display name for the instance.</span></span> <span data-ttu-id="ee344-117">Questa operazione verrà utilizzata nelle voci del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="ee344-117">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee344-118">termGrbit</span><span class="sxs-lookup"><span data-stu-id="ee344-118">termGrbit</span></span>  
    <span data-ttu-id="ee344-119">Tipo: [Microsoft. ISAM. esent. Interop. TermGrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ee344-119">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ee344-120">TermGrbit da utilizzare in fase di JetTerm.</span><span class="sxs-lookup"><span data-stu-id="ee344-120">The TermGrbit to be used at JetTerm time.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee344-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee344-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee344-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ee344-122">Reference</span></span>

[<span data-ttu-id="ee344-123">Classe dell'istanza</span><span class="sxs-lookup"><span data-stu-id="ee344-123">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="ee344-124">Membri di istanza</span><span class="sxs-lookup"><span data-stu-id="ee344-124">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="ee344-125">Overload dell'istanza</span><span class="sxs-lookup"><span data-stu-id="ee344-125">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="ee344-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ee344-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
