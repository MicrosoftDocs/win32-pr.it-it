---
description: Questa classe è la classe del tipo di evento per gli eventi di ricezione del messaggio ALPC. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: Classe ALPC_Receive_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977746"
---
# <a name="alpc_receive_message-class"></a><span data-ttu-id="0e963-104">\_Classe ALPC Receive \_ Message</span><span class="sxs-lookup"><span data-stu-id="0e963-104">ALPC\_Receive\_Message class</span></span>

<span data-ttu-id="0e963-105">Questa classe è la classe del tipo di evento per gli eventi di ricezione del messaggio ALPC.</span><span class="sxs-lookup"><span data-stu-id="0e963-105">This class is the event type class for ALPC receive message events.</span></span>

<span data-ttu-id="0e963-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="0e963-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e963-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e963-107">Syntax</span></span>

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="0e963-108">Members</span><span class="sxs-lookup"><span data-stu-id="0e963-108">Members</span></span>

<span data-ttu-id="0e963-109">La classe **ALPC \_ Receive \_ Message** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e963-109">The **ALPC\_Receive\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="0e963-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e963-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e963-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e963-111">Properties</span></span>

<span data-ttu-id="0e963-112">La classe **ALPC \_ Receive \_ Message** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e963-112">The **ALPC\_Receive\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e963-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="0e963-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e963-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e963-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e963-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e963-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e963-116">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0e963-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e963-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e963-117">Requirements</span></span>



| <span data-ttu-id="0e963-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e963-118">Requirement</span></span> | <span data-ttu-id="0e963-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0e963-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e963-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e963-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e963-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e963-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e963-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e963-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e963-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e963-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




