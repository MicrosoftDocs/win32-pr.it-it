---
description: La struttura della richiesta di i/o spaventato \_ \_ inizia una struttura delle informazioni di controllo del protocollo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: Struttura SCARD_IO_REQUEST (Winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345321"
---
# <a name="scard_io_request-structure"></a><span data-ttu-id="87cc5-103">Struttura della \_ \_ richiesta di i/o spaventato</span><span class="sxs-lookup"><span data-stu-id="87cc5-103">SCARD\_IO\_REQUEST structure</span></span>

<span data-ttu-id="87cc5-104">La struttura della **\_ \_ richiesta** di i/o spaventato inizia una struttura delle informazioni di controllo del protocollo.</span><span class="sxs-lookup"><span data-stu-id="87cc5-104">The **SCARD\_IO\_REQUEST** structure begins a protocol control information structure.</span></span> <span data-ttu-id="87cc5-105">Tutte le informazioni specifiche del protocollo seguono immediatamente la struttura.</span><span class="sxs-lookup"><span data-stu-id="87cc5-105">Any protocol-specific information then immediately follows this structure.</span></span> <span data-ttu-id="87cc5-106">L'intera lunghezza della struttura deve essere allineata con le dimensioni della parola dell'architettura hardware sottostante.</span><span class="sxs-lookup"><span data-stu-id="87cc5-106">The entire length of the structure must be aligned with the underlying hardware architecture word size.</span></span> <span data-ttu-id="87cc5-107">Ad esempio, in Win32 la lunghezza di qualsiasi informazione PCI deve essere un multiplo di quattro byte, in modo che venga allineata a un limite di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="87cc5-107">For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cc5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87cc5-108">Syntax</span></span>


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a><span data-ttu-id="87cc5-109">Members</span><span class="sxs-lookup"><span data-stu-id="87cc5-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="87cc5-110">**dwProtocol**</span><span class="sxs-lookup"><span data-stu-id="87cc5-110">**dwProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="87cc5-111">Protocollo in uso.</span><span class="sxs-lookup"><span data-stu-id="87cc5-111">Protocol in use.</span></span>

</dd> <dt>

<span data-ttu-id="87cc5-112">**cbPciLength**</span><span class="sxs-lookup"><span data-stu-id="87cc5-112">**cbPciLength**</span></span>
</dt> <dd>

<span data-ttu-id="87cc5-113">Lunghezza, in byte, della struttura della **\_ \_ richiesta** di i/o spaventato più le informazioni specifiche di PCI seguenti.</span><span class="sxs-lookup"><span data-stu-id="87cc5-113">Length, in bytes, of the **SCARD\_IO\_REQUEST** structure plus any following PCI-specific information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87cc5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87cc5-114">Requirements</span></span>



| <span data-ttu-id="87cc5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="87cc5-115">Requirement</span></span> | <span data-ttu-id="87cc5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="87cc5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87cc5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87cc5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87cc5-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="87cc5-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="87cc5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87cc5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87cc5-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87cc5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87cc5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87cc5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="87cc5-122"><dt>Winsmcrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="87cc5-122"><dt>Winsmcrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87cc5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87cc5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cc5-124">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="87cc5-124">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




