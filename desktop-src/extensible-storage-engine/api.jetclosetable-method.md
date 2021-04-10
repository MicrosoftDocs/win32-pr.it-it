---
description: 'Altre informazioni su: metodo API. JetCloseTable'
title: API. JetCloseTable, metodo
TOCTitle: 'JetCloseTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosetable(v=EXCHG.10)
ms:contentKeyID: 55100664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fee4ad7d7accf71bd4c3439f954ee36badd2ea20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966563"
---
# <a name="apijetclosetable-method"></a><span data-ttu-id="fb6ae-103">API. JetCloseTable, metodo</span><span class="sxs-lookup"><span data-stu-id="fb6ae-103">Api.JetCloseTable method</span></span>

<span data-ttu-id="fb6ae-104">Chiudere una tabella aperta.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-104">Close an open table.</span></span>

<span data-ttu-id="fb6ae-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb6ae-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fb6ae-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fb6ae-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6ae-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb6ae-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseTable ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetCloseTable(sesid, tableid)
```

``` csharp
public static void JetCloseTable(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="fb6ae-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb6ae-108">Parameters</span></span>

  - <span data-ttu-id="fb6ae-109">sesid</span><span class="sxs-lookup"><span data-stu-id="fb6ae-109">sesid</span></span>  
    <span data-ttu-id="fb6ae-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb6ae-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fb6ae-111">Sessione che ha aperto la tabella.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-111">The session which opened the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="fb6ae-112">TableID</span><span class="sxs-lookup"><span data-stu-id="fb6ae-112">tableid</span></span>  
    <span data-ttu-id="fb6ae-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb6ae-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fb6ae-114">Tabella da chiudere.</span><span class="sxs-lookup"><span data-stu-id="fb6ae-114">The table to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb6ae-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb6ae-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb6ae-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="fb6ae-116">Reference</span></span>

[<span data-ttu-id="fb6ae-117">Classe API</span><span class="sxs-lookup"><span data-stu-id="fb6ae-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fb6ae-118">Membri API</span><span class="sxs-lookup"><span data-stu-id="fb6ae-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fb6ae-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fb6ae-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
