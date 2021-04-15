---
description: Questa classe è la classe del tipo di evento per ALPC in attesa di nuovi eventi del messaggio. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: Classe ALPC_Wait_For_New_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977735"
---
# <a name="alpc_wait_for_new_message-class"></a><span data-ttu-id="dd11e-104">ALPC \_ attendere \_ la \_ nuova \_ classe Message</span><span class="sxs-lookup"><span data-stu-id="dd11e-104">ALPC\_Wait\_For\_New\_Message class</span></span>

<span data-ttu-id="dd11e-105">Questa classe è la classe del tipo di evento per ALPC in attesa di nuovi eventi del messaggio.</span><span class="sxs-lookup"><span data-stu-id="dd11e-105">This class is the event type class for ALPC wait for new message events.</span></span>

<span data-ttu-id="dd11e-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="dd11e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd11e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd11e-107">Syntax</span></span>

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a><span data-ttu-id="dd11e-108">Members</span><span class="sxs-lookup"><span data-stu-id="dd11e-108">Members</span></span>

<span data-ttu-id="dd11e-109">Il **ALPC di \_ attesa \_ per la nuova classe \_ \_ Message** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dd11e-109">The **ALPC\_Wait\_For\_New\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="dd11e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd11e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd11e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd11e-111">Properties</span></span>

<span data-ttu-id="dd11e-112">L' **\_ attesa ALPC \_ per la nuova classe \_ \_ Message** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd11e-112">The **ALPC\_Wait\_For\_New\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd11e-113">**IsServerPort**</span><span class="sxs-lookup"><span data-stu-id="dd11e-113">**IsServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd11e-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd11e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd11e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd11e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd11e-116">Indica se la porta è una porta del server.</span><span class="sxs-lookup"><span data-stu-id="dd11e-116">Indicates if the port is a server port.</span></span>

</dd> <dt>

<span data-ttu-id="dd11e-117">**PortName**</span><span class="sxs-lookup"><span data-stu-id="dd11e-117">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd11e-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd11e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd11e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd11e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd11e-120">Stringa che contiene il nome della porta su cui ALPC è in attesa.</span><span class="sxs-lookup"><span data-stu-id="dd11e-120">String that contains the name of the port on which ALPC is waiting.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd11e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd11e-121">Requirements</span></span>



| <span data-ttu-id="dd11e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd11e-122">Requirement</span></span> | <span data-ttu-id="dd11e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dd11e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd11e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd11e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dd11e-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd11e-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd11e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd11e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dd11e-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd11e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




