---
description: Le \_ costanti del flag di bit LINETERMSHARING descrivono i diversi modi in cui un terminale può essere condiviso tra dispositivi linea, indirizzi o chiamate.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Costanti LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326878"
---
# <a name="linetermsharing_-constants"></a><span data-ttu-id="351ab-103">\_Costanti LINETERMSHARING</span><span class="sxs-lookup"><span data-stu-id="351ab-103">LINETERMSHARING\_ Constants</span></span>

<span data-ttu-id="351ab-104">Le costanti del flag di bit **LINETERMSHARING \_** descrivono i diversi modi in cui un terminale può essere condiviso tra dispositivi linea, indirizzi o chiamate.</span><span class="sxs-lookup"><span data-stu-id="351ab-104">The **LINETERMSHARING\_** bit-flag constants describe different ways in which a terminal can be shared between line devices, addresses, or calls.</span></span>

<dl> <dt>

<span data-ttu-id="351ab-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privato**</span><span class="sxs-lookup"><span data-stu-id="351ab-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="351ab-106">Il dispositivo terminal è privato per un dispositivo a riga singola.</span><span class="sxs-lookup"><span data-stu-id="351ab-106">The terminal device is private to a single line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="351ab-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**\_SHAREDCONF LINETERMSHARING**</span><span class="sxs-lookup"><span data-stu-id="351ab-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING\_SHAREDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="351ab-108">Il dispositivo terminal può essere utilizzato da più righe.</span><span class="sxs-lookup"><span data-stu-id="351ab-108">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="351ab-109">Il [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) delle richieste dei diversi terminali viene unito o sottoposto a conferenza nel terminale.</span><span class="sxs-lookup"><span data-stu-id="351ab-109">The [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) requests of the various terminals end up being merged or conferenced at the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="351ab-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**\_SHAREDEXCL LINETERMSHARING**</span><span class="sxs-lookup"><span data-stu-id="351ab-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING\_SHAREDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="351ab-111">Il dispositivo terminal può essere utilizzato da più righe.</span><span class="sxs-lookup"><span data-stu-id="351ab-111">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="351ab-112">L'ultimo dispositivo a linee per eseguire un [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) o [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) nel terminale per una determinata modalità terminale avrà una connessione esclusiva al terminale per tale modalità.</span><span class="sxs-lookup"><span data-stu-id="351ab-112">The last line device to do a [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) or [**TSPI\_lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) to the terminal for a given terminal mode will have exclusive connection to the terminal for that mode.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="351ab-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="351ab-113">Remarks</span></span>

<span data-ttu-id="351ab-114">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="351ab-114">No extensibility.</span></span> <span data-ttu-id="351ab-115">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="351ab-115">All 32 bits are reserved.</span></span>

<span data-ttu-id="351ab-116">Queste costanti descrivono le classi di flussi di controllo e di informazioni che possono essere indirizzate direttamente tra un dispositivo a linee e un dispositivo Terminal (ad esempio un set di telefono).</span><span class="sxs-lookup"><span data-stu-id="351ab-116">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="351ab-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="351ab-117">Requirements</span></span>



| <span data-ttu-id="351ab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="351ab-118">Requirement</span></span> | <span data-ttu-id="351ab-119">Valore</span><span class="sxs-lookup"><span data-stu-id="351ab-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="351ab-120">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="351ab-120">TAPI version</span></span><br/> | <span data-ttu-id="351ab-121">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="351ab-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="351ab-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="351ab-122">Header</span></span><br/>       | <dl> <span data-ttu-id="351ab-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="351ab-123"><dt>Tapi.h</dt></span></span> </dl> |



 

