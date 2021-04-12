---
description: 'Altre informazioni su: costruttore di istanze (String, String)'
title: Costruttore di istanza (String, String)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344231"
---
# <a name="instance-constructor-string-string"></a><span data-ttu-id="f1b47-103">Costruttore di istanza (String, String)</span><span class="sxs-lookup"><span data-stu-id="f1b47-103">Instance constructor (String, String)</span></span>

<span data-ttu-id="f1b47-104">Inizializza una nuova istanza della classe dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f1b47-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="f1b47-105">Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="f1b47-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="f1b47-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f1b47-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f1b47-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f1b47-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b47-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1b47-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a><span data-ttu-id="f1b47-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1b47-109">Parameters</span></span>

  - <span data-ttu-id="f1b47-110">name</span><span class="sxs-lookup"><span data-stu-id="f1b47-110">name</span></span>  
    <span data-ttu-id="f1b47-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f1b47-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f1b47-112">Nome dell’istanza.</span><span class="sxs-lookup"><span data-stu-id="f1b47-112">The name of the instance.</span></span> <span data-ttu-id="f1b47-113">Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.</span><span class="sxs-lookup"><span data-stu-id="f1b47-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="f1b47-114">displayName</span><span class="sxs-lookup"><span data-stu-id="f1b47-114">displayName</span></span>  
    <span data-ttu-id="f1b47-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f1b47-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f1b47-116">Nome visualizzato per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f1b47-116">A display name for the instance.</span></span> <span data-ttu-id="f1b47-117">Questa operazione verrà utilizzata nelle voci del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="f1b47-117">This will be used in eventlog entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1b47-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1b47-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f1b47-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f1b47-119">Reference</span></span>

[<span data-ttu-id="f1b47-120">Classe dell'istanza</span><span class="sxs-lookup"><span data-stu-id="f1b47-120">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="f1b47-121">Membri di istanza</span><span class="sxs-lookup"><span data-stu-id="f1b47-121">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="f1b47-122">Overload dell'istanza</span><span class="sxs-lookup"><span data-stu-id="f1b47-122">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="f1b47-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f1b47-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
