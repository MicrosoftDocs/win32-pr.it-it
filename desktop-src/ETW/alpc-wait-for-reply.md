---
description: Questa classe è la classe del tipo di evento per ALPC in attesa di eventi di risposta. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: Classe ALPC_Wait_For_Reply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977730"
---
# <a name="alpc_wait_for_reply-class"></a><span data-ttu-id="d5a06-104">ALPC \_ attendere \_ la \_ classe Reply</span><span class="sxs-lookup"><span data-stu-id="d5a06-104">ALPC\_Wait\_For\_Reply class</span></span>

<span data-ttu-id="d5a06-105">Questa classe è la classe del tipo di evento per ALPC in attesa di eventi di risposta.</span><span class="sxs-lookup"><span data-stu-id="d5a06-105">This class is the event type class for ALPC wait for reply events.</span></span>

<span data-ttu-id="d5a06-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="d5a06-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a06-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5a06-107">Syntax</span></span>

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="d5a06-108">Members</span><span class="sxs-lookup"><span data-stu-id="d5a06-108">Members</span></span>

<span data-ttu-id="d5a06-109">La classe **ALPC \_ Wait \_ for \_ Reply** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d5a06-109">The **ALPC\_Wait\_For\_Reply** class has these types of members:</span></span>

-   [<span data-ttu-id="d5a06-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5a06-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5a06-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5a06-111">Properties</span></span>

<span data-ttu-id="d5a06-112">La classe **ALPC \_ Wait \_ for \_ Reply** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5a06-112">The **ALPC\_Wait\_For\_Reply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5a06-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="d5a06-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5a06-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5a06-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5a06-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d5a06-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5a06-116">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="d5a06-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5a06-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5a06-117">Requirements</span></span>



| <span data-ttu-id="d5a06-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5a06-118">Requirement</span></span> | <span data-ttu-id="d5a06-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d5a06-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5a06-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5a06-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a06-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5a06-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5a06-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5a06-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a06-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5a06-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




