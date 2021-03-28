---
description: Aggiorna i pulsanti indietro, avanti e fine nel frame della procedura guidata del client.
title: Metodo WebWizardHost. SetWizardButtons (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980250"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="33e1c-103">WebWizardHost. SetWizardButtons, metodo</span><span class="sxs-lookup"><span data-stu-id="33e1c-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="33e1c-104">Aggiorna i pulsanti **indietro**, **Avanti** e **fine** nel frame della procedura guidata del client.</span><span class="sxs-lookup"><span data-stu-id="33e1c-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e1c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33e1c-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="33e1c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33e1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e1c-107">*vbEnableBack* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e1c-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1c-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="33e1c-108">Type: **Boolean**</span></span>

<span data-ttu-id="33e1c-109">Abilita il pulsante **indietro** .</span><span class="sxs-lookup"><span data-stu-id="33e1c-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="33e1c-110">*vbEnableNext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e1c-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1c-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="33e1c-111">Type: **Boolean**</span></span>

<span data-ttu-id="33e1c-112">Abilita il pulsante **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="33e1c-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="33e1c-113">*vbLastPage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e1c-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e1c-114">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="33e1c-114">Type: **Boolean**</span></span>

<span data-ttu-id="33e1c-115">Abilita il pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="33e1c-115">Enables the **Finish** button.</span></span> <span data-ttu-id="33e1c-116">Indica che si tratta dell'ultima pagina sul lato server.</span><span class="sxs-lookup"><span data-stu-id="33e1c-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33e1c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="33e1c-117">Remarks</span></span>

<span data-ttu-id="33e1c-118">Assicurarsi di implementare le funzioni del gestore in ogni pagina lato server per onback () e OnNext (), corrispondenti **ai pulsanti della** procedura guidata e **successivamente**.</span><span class="sxs-lookup"><span data-stu-id="33e1c-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="33e1c-119">Le funzioni onback () e OnNext () rispondono a **SetWizardButtons**.</span><span class="sxs-lookup"><span data-stu-id="33e1c-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="33e1c-120">Al momento opportuno, la funzione OnNext () chiama **SetWizardButtons** con *vbLastPage* = **true**, che può attivare un pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="33e1c-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="33e1c-121">OnNext () chiama anche [**FinalNext**](iwebwizardhost-finalnext.md) quando un utente fa clic sul pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="33e1c-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e1c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33e1c-122">Requirements</span></span>



| <span data-ttu-id="33e1c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e1c-123">Requirement</span></span> | <span data-ttu-id="33e1c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="33e1c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33e1c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33e1c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="33e1c-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="33e1c-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="33e1c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33e1c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="33e1c-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33e1c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33e1c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33e1c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e1c-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e1c-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="33e1c-131">IDL</span><span class="sxs-lookup"><span data-stu-id="33e1c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33e1c-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33e1c-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




