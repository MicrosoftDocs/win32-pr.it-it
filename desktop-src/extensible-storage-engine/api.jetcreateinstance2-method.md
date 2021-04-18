---
description: 'Altre informazioni su: metodo API. JetCreateInstance2'
title: API. JetCreateInstance2, metodo
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d21974d5c3bd5ca6dfbab2ac493d19b202ca6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306313"
---
# <a name="apijetcreateinstance2-method"></a><span data-ttu-id="4fb4d-103">API. JetCreateInstance2, metodo</span><span class="sxs-lookup"><span data-stu-id="4fb4d-103">Api.JetCreateInstance2 method</span></span>

<span data-ttu-id="4fb4d-104">Allocare una nuova istanza del motore di database per l'utilizzo in un singolo processo, con un nome visualizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="4fb4d-104">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="4fb4d-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4fb4d-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb4d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fb4d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4fb4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fb4d-108">Parameters</span></span>

  - <span data-ttu-id="4fb4d-109">instance</span><span class="sxs-lookup"><span data-stu-id="4fb4d-109">instance</span></span>  
    <span data-ttu-id="4fb4d-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="4fb4d-111">Restituisce l'istanza appena creata.</span><span class="sxs-lookup"><span data-stu-id="4fb4d-111">Returns the newly create instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="4fb4d-112">name</span><span class="sxs-lookup"><span data-stu-id="4fb4d-112">name</span></span>  
    <span data-ttu-id="4fb4d-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4fb4d-114">Specifica un identificatore di stringa univoco per l'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="4fb4d-114">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="4fb4d-115">Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.</span><span class="sxs-lookup"><span data-stu-id="4fb4d-115">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="4fb4d-116">displayName</span><span class="sxs-lookup"><span data-stu-id="4fb4d-116">displayName</span></span>  
    <span data-ttu-id="4fb4d-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4fb4d-118">Nome visualizzato per l'istanza da creare.</span><span class="sxs-lookup"><span data-stu-id="4fb4d-118">A display name for the instance to be created.</span></span> <span data-ttu-id="4fb4d-119">Questa operazione verrà utilizzata nelle voci del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="4fb4d-119">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="4fb4d-120">grbit</span><span class="sxs-lookup"><span data-stu-id="4fb4d-120">grbit</span></span>  
    <span data-ttu-id="4fb4d-121">Tipo: [Microsoft. ISAM. esent. Interop. CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-121">Type: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4fb4d-122">Opzioni di creazione.</span><span class="sxs-lookup"><span data-stu-id="4fb4d-122">Creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fb4d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fb4d-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fb4d-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4fb4d-124">Reference</span></span>

[<span data-ttu-id="4fb4d-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="4fb4d-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4fb4d-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="4fb4d-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4fb4d-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4fb4d-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
