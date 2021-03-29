---
description: Questa classe è la classe del tipo di evento per gli eventi di fine attesa ALPC. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: Classe ALPC_Unwait
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527055"
---
# <a name="alpc_unwait-class"></a><span data-ttu-id="467c4-104">\_Classe ALPC Unwait</span><span class="sxs-lookup"><span data-stu-id="467c4-104">ALPC\_Unwait class</span></span>

<span data-ttu-id="467c4-105">Questa classe è la classe del tipo di evento per gli eventi di fine attesa ALPC.</span><span class="sxs-lookup"><span data-stu-id="467c4-105">This class is the event type class for ALPC end wait events.</span></span>

<span data-ttu-id="467c4-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="467c4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="467c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="467c4-107">Syntax</span></span>

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="467c4-108">Members</span><span class="sxs-lookup"><span data-stu-id="467c4-108">Members</span></span>

<span data-ttu-id="467c4-109">La classe **ALPC \_ Unwait** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="467c4-109">The **ALPC\_Unwait** class has these types of members:</span></span>

-   [<span data-ttu-id="467c4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="467c4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="467c4-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="467c4-111">Properties</span></span>

<span data-ttu-id="467c4-112">La classe **ALPC \_ Unwait** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="467c4-112">The **ALPC\_Unwait** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="467c4-113">**Status**</span><span class="sxs-lookup"><span data-stu-id="467c4-113">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467c4-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="467c4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="467c4-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="467c4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="467c4-116">Stato dell'operazione di attesa.</span><span class="sxs-lookup"><span data-stu-id="467c4-116">Status from wait operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="467c4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="467c4-117">Requirements</span></span>



| <span data-ttu-id="467c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="467c4-118">Requirement</span></span> | <span data-ttu-id="467c4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="467c4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="467c4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="467c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="467c4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="467c4-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="467c4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="467c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="467c4-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="467c4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




