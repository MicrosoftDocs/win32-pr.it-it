---
description: Questa classe è la classe del tipo di evento per gli eventi di invio del messaggio ALPC. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: Classe ALPC_Send_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130007"
---
# <a name="alpc_send_message-class"></a><span data-ttu-id="ace9e-104">\_Classe ALPC Send \_ Message</span><span class="sxs-lookup"><span data-stu-id="ace9e-104">ALPC\_Send\_Message class</span></span>

<span data-ttu-id="ace9e-105">Questa classe è la classe del tipo di evento per gli eventi di invio del messaggio ALPC.</span><span class="sxs-lookup"><span data-stu-id="ace9e-105">This class is the event type class for ALPC send message events.</span></span>

<span data-ttu-id="ace9e-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="ace9e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace9e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ace9e-107">Syntax</span></span>

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="ace9e-108">Members</span><span class="sxs-lookup"><span data-stu-id="ace9e-108">Members</span></span>

<span data-ttu-id="ace9e-109">La classe **ALPC \_ Send \_ Message** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ace9e-109">The **ALPC\_Send\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="ace9e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ace9e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ace9e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ace9e-111">Properties</span></span>

<span data-ttu-id="ace9e-112">La classe di **\_ invio del \_ messaggio ALPC** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ace9e-112">The **ALPC\_Send\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ace9e-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="ace9e-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ace9e-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ace9e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ace9e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ace9e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ace9e-116">Identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ace9e-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ace9e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ace9e-117">Requirements</span></span>



| <span data-ttu-id="ace9e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace9e-118">Requirement</span></span> | <span data-ttu-id="ace9e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ace9e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ace9e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace9e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ace9e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ace9e-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ace9e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace9e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ace9e-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ace9e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




