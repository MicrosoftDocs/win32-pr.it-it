---
description: Le \_ costanti LINETONEMODE descrivono selezioni diverse che vengono usate durante la generazione di toni di riga.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Costanti LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325284"
---
# <a name="linetonemode_-constants"></a><span data-ttu-id="5e7d7-103">\_Costanti LINETONEMODE</span><span class="sxs-lookup"><span data-stu-id="5e7d7-103">LINETONEMODE\_ Constants</span></span>

<span data-ttu-id="5e7d7-104">Le **\_ costanti LINETONEMODE** descrivono selezioni diverse che vengono usate durante la generazione di toni di riga.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-104">The **LINETONEMODE\_ constants** describe different selections that are used when generating line tones.</span></span>

<dl> <dt>

<span data-ttu-id="5e7d7-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**\_segnale acustico LINETONEMODE**</span><span class="sxs-lookup"><span data-stu-id="5e7d7-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE\_BEEP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e7d7-106">Il tono è un segnale acustico, ad esempio quello usato per annunciare l'inizio di una registrazione.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-106">The tone is a beep, such as that used to announce the beginning of a recording.</span></span> <span data-ttu-id="5e7d7-107">La definizione esatta è il provider di servizi definito.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-107">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e7d7-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**\_fatturazione LINETONEMODE**</span><span class="sxs-lookup"><span data-stu-id="5e7d7-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE\_BILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e7d7-109">Il tono è un tono di informazioni sulla fatturazione, ad esempio un tono di richiesta della carta di credito.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-109">The tone is a billing information tone such as a credit card prompt tone.</span></span> <span data-ttu-id="5e7d7-110">La definizione esatta è il provider di servizi definito.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-110">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e7d7-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="5e7d7-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e7d7-112">Il tono è un tono occupato.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-112">The tone is a busy tone.</span></span> <span data-ttu-id="5e7d7-113">La definizione esatta è il provider di servizi definito.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-113">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e7d7-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personalizzato**</span><span class="sxs-lookup"><span data-stu-id="5e7d7-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e7d7-115">Il tono è un tono personalizzato definito dalle frequenze dei componenti, di tipo [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span><span class="sxs-lookup"><span data-stu-id="5e7d7-115">The tone is a custom tone defined by its component frequencies, of type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5e7d7-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE \_ risponder**</span><span class="sxs-lookup"><span data-stu-id="5e7d7-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5e7d7-117">Il tono è la risponder.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-117">The tone is ringback tone.</span></span> <span data-ttu-id="5e7d7-118">La definizione esatta è il provider di servizi definito.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-118">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e7d7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e7d7-119">Remarks</span></span>

<span data-ttu-id="5e7d7-120">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-120">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="5e7d7-121">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-121">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="5e7d7-122">Queste costanti vengono usate per definire i toni da generare inband su una chiamata alla parte remota.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-122">These constants are used to define tones to be generated inband over a call to the remote party.</span></span> <span data-ttu-id="5e7d7-123">Si noti che il rilevamento dei toni non personalizzati non usa queste costanti.</span><span class="sxs-lookup"><span data-stu-id="5e7d7-123">Note that tone detection of non-custom tones does not use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e7d7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e7d7-124">Requirements</span></span>



| <span data-ttu-id="5e7d7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7d7-125">Requirement</span></span> | <span data-ttu-id="5e7d7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5e7d7-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5e7d7-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5e7d7-127">TAPI version</span></span><br/> | <span data-ttu-id="5e7d7-128">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5e7d7-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5e7d7-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e7d7-129">Header</span></span><br/>       | <dl> <span data-ttu-id="5e7d7-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e7d7-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




