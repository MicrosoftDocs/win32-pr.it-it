---
description: Le \_ costanti del flag di bit PHONEHOOKSWITCHDEV descrivono i vari dispositivi di I/O audio ognuno con il proprio hookswitch controllabile dal computer.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Costanti PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333948"
---
# <a name="phonehookswitchdev_-constants"></a><span data-ttu-id="e3c4f-103">\_Costanti PHONEHOOKSWITCHDEV</span><span class="sxs-lookup"><span data-stu-id="e3c4f-103">PHONEHOOKSWITCHDEV\_ Constants</span></span>

<span data-ttu-id="e3c4f-104">Le costanti del flag di bit **PHONEHOOKSWITCHDEV \_** descrivono i vari dispositivi di I/O audio ognuno con il proprio hookswitch controllabile dal computer.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-104">The **PHONEHOOKSWITCHDEV\_** bit-flag constants describe various audio I/O devices each with its own hookswitch controllable from the computer.</span></span>

<dl> <dt>

<span data-ttu-id="e3c4f-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV \_ portatile**</span><span class="sxs-lookup"><span data-stu-id="e3c4f-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV\_HANDSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3c4f-106">Si tratta di un telefono auricolare e di un Bocchino standard.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-106">This is a standard ear- and mouthpiece phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3c4f-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**\_auricolare PHONEHOOKSWITCHDEV**</span><span class="sxs-lookup"><span data-stu-id="e3c4f-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV\_HEADSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3c4f-108">Si tratta di un auricolare connesso al set di telefono.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-108">This is a headset connected to the phone set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3c4f-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ speaker**</span><span class="sxs-lookup"><span data-stu-id="e3c4f-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3c4f-110">Si tratta di un altoparlante e microfono incorporato.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-110">This is a built-in loudspeaker and microphone.</span></span> <span data-ttu-id="e3c4f-111">Potrebbe anche trattarsi di un altoparlante aggiuntivo collegato esternamente al set telefonico.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-111">This could also be an externally connected adjunct speaker to the telephone set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3c4f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3c4f-112">Remarks</span></span>

<span data-ttu-id="e3c4f-113">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-113">No extensibility.</span></span> <span data-ttu-id="e3c4f-114">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="e3c4f-115">Queste costanti vengono usate nella struttura dei dati [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) per indicare le funzionalità del dispositivo hookswitch di un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-115">These constants are used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to indicate the hookswitch device capabilities of a phone device.</span></span> <span data-ttu-id="e3c4f-116">La struttura [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) segnala lo stato dei dispositivi hookswitch del telefono.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-116">The [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) structure reports the state of the phone's hookswitch devices.</span></span> <span data-ttu-id="e3c4f-117">La funzione [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) e [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) lo usano come parametro per selezionare il dispositivo di i/O del telefono.</span><span class="sxs-lookup"><span data-stu-id="e3c4f-117">The function [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) and [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) use it as a parameter to select the phone's I/O device.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c4f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3c4f-118">Requirements</span></span>



| <span data-ttu-id="e3c4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3c4f-119">Requirement</span></span> | <span data-ttu-id="e3c4f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c4f-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e3c4f-121">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e3c4f-121">TAPI version</span></span><br/> | <span data-ttu-id="e3c4f-122">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e3c4f-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e3c4f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3c4f-123">Header</span></span><br/>       | <dl> <span data-ttu-id="e3c4f-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c4f-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




