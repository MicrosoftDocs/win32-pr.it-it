---
description: 'Altre informazioni su: costruttore di istanza (stringa)'
title: Costruttore di istanza (String)
TOCTitle: Instance constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103263
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
ms.openlocfilehash: 8cf184fc9b8d921b1d8bd1003b960bc65a6ffb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234251"
---
# <a name="instance-constructor-string"></a><span data-ttu-id="8b3c4-103">Costruttore di istanza (String)</span><span class="sxs-lookup"><span data-stu-id="8b3c4-103">Instance constructor (String)</span></span>

<span data-ttu-id="8b3c4-104">Inizializza una nuova istanza della classe dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8b3c4-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="8b3c4-105">Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="8b3c4-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="8b3c4-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8b3c4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8b3c4-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8b3c4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3c4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b3c4-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String _
)
'Usage
Dim name As String

Dim instance As New Instance(name)
```

``` csharp
public Instance(
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="8b3c4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b3c4-109">Parameters</span></span>

  - <span data-ttu-id="8b3c4-110">name</span><span class="sxs-lookup"><span data-stu-id="8b3c4-110">name</span></span>  
    <span data-ttu-id="8b3c4-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8b3c4-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8b3c4-112">Nome dell’istanza.</span><span class="sxs-lookup"><span data-stu-id="8b3c4-112">The name of the instance.</span></span> <span data-ttu-id="8b3c4-113">Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.</span><span class="sxs-lookup"><span data-stu-id="8b3c4-113">This string must be unique within a given process hosting the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b3c4-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b3c4-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8b3c4-115">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8b3c4-115">Reference</span></span>

[<span data-ttu-id="8b3c4-116">Classe dell'istanza</span><span class="sxs-lookup"><span data-stu-id="8b3c4-116">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="8b3c4-117">Membri di istanza</span><span class="sxs-lookup"><span data-stu-id="8b3c4-117">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="8b3c4-118">Overload dell'istanza</span><span class="sxs-lookup"><span data-stu-id="8b3c4-118">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="8b3c4-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8b3c4-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
