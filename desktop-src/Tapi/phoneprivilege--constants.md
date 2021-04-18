---
description: Le \_ costanti del flag di bit PHONEPRIVILEGE descrivono i vari modi in cui è possibile aprire un dispositivo telefonico.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Costanti PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333938"
---
# <a name="phoneprivilege_-constants"></a><span data-ttu-id="e694d-103">\_Costanti PHONEPRIVILEGE</span><span class="sxs-lookup"><span data-stu-id="e694d-103">PHONEPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="e694d-104">Le costanti del flag di bit **PHONEPRIVILEGE \_** descrivono i vari modi in cui è possibile aprire un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="e694d-104">The **PHONEPRIVILEGE\_** bit-flag constants describe the various ways in which a phone device can be opened.</span></span>

<dl> <dt>

<span data-ttu-id="e694d-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**\_monitoraggio PHONEPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="e694d-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e694d-106">Un'applicazione che apre un dispositivo telefonico con il privilegio di monitoraggio viene aggiornata sugli eventi e sulle modifiche di stato che si verificano sul telefono.</span><span class="sxs-lookup"><span data-stu-id="e694d-106">An application that opens a phone device with the monitor privilege is informed about events and state changes occurring on the phone.</span></span> <span data-ttu-id="e694d-107">L'applicazione non è in grado di richiamare alcuna operazione sul dispositivo telefonico che cambierebbe lo stato, quindi possono essere richiamate solo le operazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="e694d-107">The application cannot invoke any operations on the phone device that would change its state, so only status operations can be invoked.</span></span> <span data-ttu-id="e694d-108">Più applicazioni possono monitorare un dispositivo telefonico in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="e694d-108">Multiple applications can monitor a phone device at any given time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e694d-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**\_proprietario PHONEPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="e694d-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e694d-110">Un'applicazione che apre un dispositivo telefonico con il privilegio proprietario è autorizzata a modificare lo stato dei blocchi di lampade, suoneria, schermo, hookswitch e dati del telefono.</span><span class="sxs-lookup"><span data-stu-id="e694d-110">An application that opens a phone device with the owner privilege is allowed to change the state of the lamps, ringer, display, hookswitch, and data blocks of the phone.</span></span> <span data-ttu-id="e694d-111">L'apertura di un dispositivo telefonico in modalità proprietario fornisce anche il monitoraggio del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="e694d-111">Opening a phone device in owner mode also provides monitoring of the phone device.</span></span> <span data-ttu-id="e694d-112">Una sola applicazione può essere il proprietario di un dispositivo telefonico in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="e694d-112">Only one application is allowed to be the owner of a phone device at any given time.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e694d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e694d-113">Remarks</span></span>

<span data-ttu-id="e694d-114">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="e694d-114">No extensibility.</span></span> <span data-ttu-id="e694d-115">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="e694d-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e694d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e694d-116">Requirements</span></span>



| <span data-ttu-id="e694d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e694d-117">Requirement</span></span> | <span data-ttu-id="e694d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e694d-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e694d-119">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e694d-119">TAPI version</span></span><br/> | <span data-ttu-id="e694d-120">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e694d-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e694d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e694d-121">Header</span></span><br/>       | <dl> <span data-ttu-id="e694d-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e694d-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




