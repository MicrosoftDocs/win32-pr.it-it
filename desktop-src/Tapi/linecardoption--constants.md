---
description: Le \_ costanti LINECARDOPTION definiscono i valori usati nel membro dwOptions della struttura LINECARDENTRY restituita come parte della struttura LINETRANSLATECAPS restituita da lineGetTranslateCaps.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: Costanti LINECARDOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333651"
---
# <a name="linecardoption_-constants"></a><span data-ttu-id="fc613-103">\_Costanti LINECARDOPTION</span><span class="sxs-lookup"><span data-stu-id="fc613-103">LINECARDOPTION\_ Constants</span></span>

<span data-ttu-id="fc613-104">Le **\_ costanti LINECARDOPTION** definiscono i valori usati nel membro **dwOptions** della struttura [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) restituita come parte della struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) restituita da [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="fc613-104">The **LINECARDOPTION\_constants** define values used in the **dwOptions** member of the [**LINECARDENTRY**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span> <span data-ttu-id="fc613-105">Le **\_ costanti LINECARDOPTION** t hanno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc613-105">The **LINECARDOPTION\_constants** t has the following values:</span></span>

<dl> <dt>

<span data-ttu-id="fc613-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION \_ nascosto**</span><span class="sxs-lookup"><span data-stu-id="fc613-106"><span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**LINECARDOPTION\_HIDDEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc613-107">Questa scheda chiamante è stata nascosta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="fc613-107">This calling card has been hidden by the user.</span></span> <span data-ttu-id="fc613-108">Non viene visualizzato da dial Helper nell'elenco principale delle schede di chiamata disponibili, ma verrà visualizzato nell'elenco di schede da cui è possibile copiare le regole di composizione.</span><span class="sxs-lookup"><span data-stu-id="fc613-108">It is not shown by Dial Helper in the main listing of available calling cards, but will be shown in the list of cards from which dialing rules can be copied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc613-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="fc613-109"><span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**LINECARDOPTION\_PREDEFINED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc613-110">Questa scheda chiamante è una delle definizioni delle schede di chiamata predefinite incluse in telefonia da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fc613-110">This calling card is one of the predefined calling card definitions included with Telephony by Microsoft.</span></span> <span data-ttu-id="fc613-111">Non è possibile rimuoverlo completamente utilizzando l'helper di connessione. Se l'utente tenta di rimuoverlo, viene nascosto.</span><span class="sxs-lookup"><span data-stu-id="fc613-111">It cannot be removed entirely using Dial Helper; if the user attempts to remove it, it will become HIDDEN.</span></span> <span data-ttu-id="fc613-112">Continua quindi a essere accessibile per la copia delle regole di composizione.</span><span class="sxs-lookup"><span data-stu-id="fc613-112">It thus continues to be accessible for copying of dialing rules.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc613-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc613-113">Remarks</span></span>

<span data-ttu-id="fc613-114">Non estendibile.</span><span class="sxs-lookup"><span data-stu-id="fc613-114">Not extensible.</span></span> <span data-ttu-id="fc613-115">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="fc613-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc613-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc613-116">Requirements</span></span>



| <span data-ttu-id="fc613-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc613-117">Requirement</span></span> | <span data-ttu-id="fc613-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fc613-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fc613-119">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="fc613-119">TAPI version</span></span><br/> | <span data-ttu-id="fc613-120">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fc613-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fc613-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc613-121">Header</span></span><br/>       | <dl> <span data-ttu-id="fc613-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc613-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




