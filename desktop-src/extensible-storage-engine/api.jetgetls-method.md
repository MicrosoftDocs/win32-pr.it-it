---
description: 'Altre informazioni su: metodo API. JetGetLS'
title: API. JetGetLS, metodo
TOCTitle: 'JetGetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS@,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetls(v=EXCHG.10)
ms:contentKeyID: 55100734
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611f92e21dad83121b4e4a6226838ac9ebce2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225991"
---
# <a name="apijetgetls-method"></a><span data-ttu-id="32837-103">API. JetGetLS, metodo</span><span class="sxs-lookup"><span data-stu-id="32837-103">Api.JetGetLS method</span></span>

<span data-ttu-id="32837-104">Consente all'applicazione di recuperare l'handle di contesto noto come archivio locale associato a un cursore o alla tabella associata a tale cursore.</span><span class="sxs-lookup"><span data-stu-id="32837-104">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="32837-105">Questo handle di contesto deve essere stato impostato in precedenza tramite [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="32837-105">This context handle must have been previously set using [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span> <span data-ttu-id="32837-106">JetGetLS può essere utilizzato anche per recuperare contemporaneamente l'handle del contesto corrente per un cursore o una tabella e reimpostare tale handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="32837-106">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="32837-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="32837-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="32837-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="32837-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="32837-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32837-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetGetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetGetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="32837-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="32837-110">Parameters</span></span>

  - <span data-ttu-id="32837-111">sesid</span><span class="sxs-lookup"><span data-stu-id="32837-111">sesid</span></span>  
    <span data-ttu-id="32837-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="32837-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="32837-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="32837-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="32837-114">TableID</span><span class="sxs-lookup"><span data-stu-id="32837-114">tableid</span></span>  
    <span data-ttu-id="32837-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="32837-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="32837-116">Cursore da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="32837-116">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="32837-117">ls</span><span class="sxs-lookup"><span data-stu-id="32837-117">ls</span></span>  
    <span data-ttu-id="32837-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="32837-118">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="32837-119">Restituisce l'handle di contesto recuperato.</span><span class="sxs-lookup"><span data-stu-id="32837-119">Returns the retrieved context handle.</span></span>

<!-- end list -->

  - <span data-ttu-id="32837-120">grbit</span><span class="sxs-lookup"><span data-stu-id="32837-120">grbit</span></span>  
    <span data-ttu-id="32837-121">Tipo: [Microsoft. ISAM. esent. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="32837-121">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="32837-122">Recupera le opzioni.</span><span class="sxs-lookup"><span data-stu-id="32837-122">Retrieve options.</span></span>

## <a name="see-also"></a><span data-ttu-id="32837-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32837-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="32837-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="32837-124">Reference</span></span>

[<span data-ttu-id="32837-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="32837-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="32837-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="32837-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="32837-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="32837-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
