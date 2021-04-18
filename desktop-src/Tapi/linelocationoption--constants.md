---
description: Le \_ costanti LINELOCATIONOPTION definiscono i valori usati nel membro dwOptions della struttura LINELOCATIONENTRY restituita come parte della struttura LINETRANSLATECAPS restituita da lineGetTranslateCaps.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: Costanti LINELOCATIONOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331027"
---
# <a name="linelocationoption_-constants"></a><span data-ttu-id="9e0e5-103">\_Costanti LINELOCATIONOPTION</span><span class="sxs-lookup"><span data-stu-id="9e0e5-103">LINELOCATIONOPTION\_ Constants</span></span>

<span data-ttu-id="9e0e5-104">Le **costanti \_ LINELOCATIONOPTION** definiscono i valori usati nel membro **dwOptions** della struttura [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) restituita come parte della struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) restituita da [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span><span class="sxs-lookup"><span data-stu-id="9e0e5-104">The **LINELOCATIONOPTION\_** constants define values used in the **dwOptions** member of the [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span>

<dl> <dt>

<span data-ttu-id="9e0e5-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**\_PULSEDIAL LINELOCATIONOPTION**</span><span class="sxs-lookup"><span data-stu-id="9e0e5-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION\_PULSEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9e0e5-106">La modalità di composizione predefinita in questa posizione è la composizione a impulsi.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-106">The default dialing mode at this location is pulse dialing.</span></span> <span data-ttu-id="9e0e5-107">Se questo bit è impostato, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) inserirà un modificatore di composizione "P" all'inizio della stringa di connessione remota restituita quando si seleziona questa posizione.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-107">If this bit is set, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) will insert a "P" dial modifier at the beginning of the dialable string returned when this location is selected.</span></span> <span data-ttu-id="9e0e5-108">Se questo bit non è impostato, **lineTranslateAddress** inserirà un modificatore di composizione "T" all'inizio della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-108">If this bit is not set, **lineTranslateAddress** will insert a "T" dial modifier at the beginning of the dialable string.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e0e5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e0e5-109">Remarks</span></span>

<span data-ttu-id="9e0e5-110">Non estendibile.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-110">Not extensible.</span></span> <span data-ttu-id="9e0e5-111">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="9e0e5-111">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0e5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e0e5-112">Requirements</span></span>



| <span data-ttu-id="9e0e5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e0e5-113">Requirement</span></span> | <span data-ttu-id="9e0e5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9e0e5-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9e0e5-115">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="9e0e5-115">TAPI version</span></span><br/> | <span data-ttu-id="9e0e5-116">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9e0e5-116">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9e0e5-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e0e5-117">Header</span></span><br/>       | <dl> <span data-ttu-id="9e0e5-118"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e0e5-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




