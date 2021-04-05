---
description: Usato con il \_ \_ codice di controllo ioctl SCSI miniport IOCTL e CTLCODE \_ ISCSITGT \_ SPT \_ Session \_ End (0x101) per arrestare una sessione.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Struttura ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "103886064"
---
# <a name="iscsitgt_spt_session_stop-structure"></a><span data-ttu-id="01a1b-103">\_Struttura di \_ arresto della sessione ISCSITGT SPT \_</span><span class="sxs-lookup"><span data-stu-id="01a1b-103">ISCSITGT\_SPT\_SESSION\_STOP structure</span></span>

<span data-ttu-id="01a1b-104">\[La struttura seguente è disponibile per l'uso in Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="01a1b-104">\[The following structure is available for use in Windows Server 2012 R2.</span></span> <span data-ttu-id="01a1b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="01a1b-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="01a1b-106">Usato con il codice di controllo IOCTL [**\_ SCSI \_ Miniport**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL e CTLCODE \_ ISCSITGT \_ SPT \_ Session \_ End (0x101) per arrestare una sessione.</span><span class="sxs-lookup"><span data-stu-id="01a1b-106">Used with the [**IOCTL\_SCSI\_MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL and the CTLCODE\_ISCSITGT\_SPT\_SESSION\_END (0x101) control code to stop a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a1b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01a1b-107">Syntax</span></span>


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a><span data-ttu-id="01a1b-108">Members</span><span class="sxs-lookup"><span data-stu-id="01a1b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="01a1b-109">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="01a1b-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="01a1b-110">Intestazione obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="01a1b-110">Mandatory header.</span></span>

</dd> <dt>

<span data-ttu-id="01a1b-111">**ITNexusHandle**</span><span class="sxs-lookup"><span data-stu-id="01a1b-111">**ITNexusHandle**</span></span>
</dt> <dd>

<span data-ttu-id="01a1b-112">Handle opaco che rappresenta una sessione.</span><span class="sxs-lookup"><span data-stu-id="01a1b-112">An opaque handle representing a session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01a1b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01a1b-113">Requirements</span></span>



| <span data-ttu-id="01a1b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a1b-114">Requirement</span></span> | <span data-ttu-id="01a1b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="01a1b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="01a1b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a1b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01a1b-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="01a1b-117">None supported</span></span><br/>                               |
| <span data-ttu-id="01a1b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a1b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01a1b-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="01a1b-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="01a1b-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="01a1b-120">End of client support</span></span><br/>    | <span data-ttu-id="01a1b-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="01a1b-121">None supported</span></span><br/>                               |
| <span data-ttu-id="01a1b-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="01a1b-122">End of server support</span></span><br/>    | <span data-ttu-id="01a1b-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="01a1b-123">Windows Server 2012 R2</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="01a1b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01a1b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a1b-125">Pass-through di destinazione iSCSI</span><span class="sxs-lookup"><span data-stu-id="01a1b-125">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="01a1b-126">**\_controllo di io SRB \_**</span><span class="sxs-lookup"><span data-stu-id="01a1b-126">**SRB\_IO\_CONTROL**</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
