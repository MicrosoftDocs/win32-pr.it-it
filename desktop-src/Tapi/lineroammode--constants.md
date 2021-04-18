---
description: Le \_ costanti del flag di bit LINEROAMMODE descrivono lo stato di roaming di un dispositivo a linee.
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: Costanti LINEROAMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326883"
---
# <a name="lineroammode_-constants"></a><span data-ttu-id="d7c37-103">\_Costanti LINEROAMMODE</span><span class="sxs-lookup"><span data-stu-id="d7c37-103">LINEROAMMODE\_ Constants</span></span>

<span data-ttu-id="d7c37-104">Le costanti del flag di bit **LINEROAMMODE \_** descrivono lo stato di roaming di un dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="d7c37-104">The **LINEROAMMODE\_** bit-flag constants describe the roaming status of a line device.</span></span>

<dl> <dt>

<span data-ttu-id="d7c37-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**\_Home page di LINEROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="d7c37-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE\_HOME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d7c37-106">La riga è connessa al nodo della rete domestica.</span><span class="sxs-lookup"><span data-stu-id="d7c37-106">The line is connected to the home network node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7c37-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**\_ROAMA LINEROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="d7c37-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE\_ROAMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d7c37-108">La linea è connessa al gestore di roaming e le chiamate vengono addebitate di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="d7c37-108">The line is connected to the Roam-A carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7c37-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**\_ROAMB LINEROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="d7c37-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE\_ROAMB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d7c37-110">La linea è connessa al gestore di roaming B e le chiamate vengono addebitate di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="d7c37-110">The line is connected to the Roam-B carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7c37-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="d7c37-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d7c37-112">La modalità Roam non è disponibile e non sarà nota.</span><span class="sxs-lookup"><span data-stu-id="d7c37-112">The roam mode is unavailable and will not be known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7c37-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="d7c37-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d7c37-114">La modalità Roam è attualmente sconosciuta, ma potrebbe essere nota in seguito.</span><span class="sxs-lookup"><span data-stu-id="d7c37-114">The roam mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7c37-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7c37-115">Remarks</span></span>

<span data-ttu-id="d7c37-116">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="d7c37-116">No extensibility.</span></span> <span data-ttu-id="d7c37-117">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="d7c37-117">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c37-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7c37-118">Requirements</span></span>



| <span data-ttu-id="d7c37-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7c37-119">Requirement</span></span> | <span data-ttu-id="d7c37-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d7c37-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d7c37-121">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d7c37-121">TAPI version</span></span><br/> | <span data-ttu-id="d7c37-122">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d7c37-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d7c37-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7c37-123">Header</span></span><br/>       | <dl> <span data-ttu-id="d7c37-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c37-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




