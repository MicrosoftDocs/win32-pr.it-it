---
description: Le \_ costanti del flag di bit LINETRANSFERMODE descrivono diverse modalità di risoluzione delle richieste di trasferimento delle chiamate.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Costanti LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325281"
---
# <a name="linetransfermode_-constants"></a><span data-ttu-id="b6613-103">\_Costanti LINETRANSFERMODE</span><span class="sxs-lookup"><span data-stu-id="b6613-103">LINETRANSFERMODE\_ Constants</span></span>

<span data-ttu-id="b6613-104">Le costanti del flag di bit **LINETRANSFERMODE \_** descrivono diverse modalità di risoluzione delle richieste di trasferimento delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="b6613-104">The **LINETRANSFERMODE\_** bit-flag constants describe different ways of resolving call transfer requests.</span></span>

<dl> <dt>

<span data-ttu-id="b6613-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_conferenza LINETRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="b6613-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6613-106">Il trasferimento viene risolto stabilendo una conferenza a tre vie tra l'applicazione, l'entità connessa alla chiamata iniziale e l'entità connessa alla chiamata di consultazione.</span><span class="sxs-lookup"><span data-stu-id="b6613-106">The transfer is resolved by establishing a three-way conference between the application, the party connected to the initial call, and the party connected to the consultation call.</span></span> <span data-ttu-id="b6613-107">Quando questa opzione è selezionata, viene creata una chiamata di conferenza.</span><span class="sxs-lookup"><span data-stu-id="b6613-107">A conference call is created when this option is selected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6613-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_trasferimento LINETRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="b6613-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b6613-109">Il trasferimento viene risolto trasferendo la chiamata iniziale alla chiamata di consultazione.</span><span class="sxs-lookup"><span data-stu-id="b6613-109">The transfer is resolved by transferring the initial call to the consultation call.</span></span> <span data-ttu-id="b6613-110">Entrambe le chiamate diventeranno inattive per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6613-110">Both calls will become idle to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6613-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6613-111">Remarks</span></span>

<span data-ttu-id="b6613-112">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="b6613-112">No extensibility.</span></span> <span data-ttu-id="b6613-113">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="b6613-113">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6613-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6613-114">Requirements</span></span>



| <span data-ttu-id="b6613-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6613-115">Requirement</span></span> | <span data-ttu-id="b6613-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b6613-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b6613-117">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b6613-117">TAPI version</span></span><br/> | <span data-ttu-id="b6613-118">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b6613-118">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b6613-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6613-119">Header</span></span><br/>       | <dl> <span data-ttu-id="b6613-120"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6613-120"><dt>Tapi.h</dt></span></span> </dl> |



 

 




