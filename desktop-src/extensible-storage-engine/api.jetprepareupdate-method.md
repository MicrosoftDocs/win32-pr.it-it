---
description: 'Altre informazioni su: metodo API. JetPrepareUpdate'
title: API. JetPrepareUpdate, metodo
TOCTitle: 'JetPrepareUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetprepareupdate(v=EXCHG.10)
ms:contentKeyID: 55100782
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8094fef5fcf008dd5f6eb6f2bfd05a0be1bf077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233781"
---
# <a name="apijetprepareupdate-method"></a><span data-ttu-id="94388-103">API. JetPrepareUpdate, metodo</span><span class="sxs-lookup"><span data-stu-id="94388-103">Api.JetPrepareUpdate method</span></span>

<span data-ttu-id="94388-104">Preparare un cursore per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="94388-104">Prepare a cursor for update.</span></span>

<span data-ttu-id="94388-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="94388-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="94388-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="94388-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="94388-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94388-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrepareUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prepApi.JetPrepareUpdate(sesid, tableid, _
    prep)
```

``` csharp
public static void JetPrepareUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="94388-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="94388-108">Parameters</span></span>

  - <span data-ttu-id="94388-109">sesid</span><span class="sxs-lookup"><span data-stu-id="94388-109">sesid</span></span>  
    <span data-ttu-id="94388-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="94388-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="94388-111">Sessione che avvia l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="94388-111">The session which is starting the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="94388-112">TableID</span><span class="sxs-lookup"><span data-stu-id="94388-112">tableid</span></span>  
    <span data-ttu-id="94388-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="94388-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="94388-114">Cursore per il quale avviare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="94388-114">The cursor to start the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="94388-115">Prep</span><span class="sxs-lookup"><span data-stu-id="94388-115">prep</span></span>  
    <span data-ttu-id="94388-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="94388-116">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="94388-117">Tipo di aggiornamento da preparare.</span><span class="sxs-lookup"><span data-stu-id="94388-117">The type of update to prepare.</span></span>

## <a name="see-also"></a><span data-ttu-id="94388-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94388-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="94388-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="94388-119">Reference</span></span>

[<span data-ttu-id="94388-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="94388-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="94388-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="94388-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="94388-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="94388-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
