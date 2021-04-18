---
description: 'Altre informazioni su: costruttore di aggiornamento'
title: Aggiorna Costruttore
TOCTitle: 'Update constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.update(v=EXCHG.10)
ms:contentKeyID: 55104189
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.Update
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 841403523e0cae7c71fb8fa0861c1d400a26a726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316920"
---
# <a name="update-constructor"></a><span data-ttu-id="dc993-103">Aggiorna Costruttore</span><span class="sxs-lookup"><span data-stu-id="dc993-103">Update constructor</span></span>

<span data-ttu-id="dc993-104">Inizializza una nuova istanza della classe Update.</span><span class="sxs-lookup"><span data-stu-id="dc993-104">Initializes a new instance of the Update class.</span></span> <span data-ttu-id="dc993-105">Viene avviato automaticamente un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="dc993-105">This automatically begins an update.</span></span> <span data-ttu-id="dc993-106">Se non viene salvato in modo esplicito, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="dc993-106">The update will be cancelled if not explicitly saved.</span></span>

<span data-ttu-id="dc993-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc993-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dc993-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc993-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc993-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc993-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prep

Dim instance As New Update(sesid, tableid, _
    prep)
```

``` csharp
public Update(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="dc993-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc993-110">Parameters</span></span>

  - <span data-ttu-id="dc993-111">sesid</span><span class="sxs-lookup"><span data-stu-id="dc993-111">sesid</span></span>  
    <span data-ttu-id="dc993-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dc993-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dc993-113">Sessione per la quale avviare la transazione.</span><span class="sxs-lookup"><span data-stu-id="dc993-113">The session to start the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc993-114">TableID</span><span class="sxs-lookup"><span data-stu-id="dc993-114">tableid</span></span>  
    <span data-ttu-id="dc993-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dc993-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dc993-116">TableID per cui preparare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="dc993-116">The tableid to prepare the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="dc993-117">Prep</span><span class="sxs-lookup"><span data-stu-id="dc993-117">prep</span></span>  
    <span data-ttu-id="dc993-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dc993-118">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="dc993-119">Tipo di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="dc993-119">The type of update.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc993-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc993-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc993-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="dc993-121">Reference</span></span>

[<span data-ttu-id="dc993-122">Classe Update</span><span class="sxs-lookup"><span data-stu-id="dc993-122">Update class</span></span>](./update-class.md)

[<span data-ttu-id="dc993-123">Aggiornare i membri</span><span class="sxs-lookup"><span data-stu-id="dc993-123">Update members</span></span>](./update-members.md)

[<span data-ttu-id="dc993-124">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dc993-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
