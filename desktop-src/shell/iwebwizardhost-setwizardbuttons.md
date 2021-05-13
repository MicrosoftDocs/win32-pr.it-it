---
description: Aggiorna i pulsanti Indietro, Avanti e Fine nel frame della procedura guidata del client.
title: Metodo WebWizardHost.SetWizardButtons (Shldisp.h)
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
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842622"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="fc933-103">Metodo WebWizardHost.SetWizardButtons</span><span class="sxs-lookup"><span data-stu-id="fc933-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="fc933-104">Aggiorna i **pulsanti Indietro** **,** Avanti **e** Fine nel frame della procedura guidata del client.</span><span class="sxs-lookup"><span data-stu-id="fc933-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc933-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc933-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="fc933-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc933-107">*vbEnableBack* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fc933-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc933-108">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc933-108">Type: **Boolean**</span></span>

<span data-ttu-id="fc933-109">Abilita il **pulsante** Indietro.</span><span class="sxs-lookup"><span data-stu-id="fc933-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="fc933-110">*vbEnableNext* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fc933-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc933-111">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc933-111">Type: **Boolean**</span></span>

<span data-ttu-id="fc933-112">Abilita il pulsante **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="fc933-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="fc933-113">*vbLastPage* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fc933-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc933-114">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc933-114">Type: **Boolean**</span></span>

<span data-ttu-id="fc933-115">Abilita il **pulsante** Fine.</span><span class="sxs-lookup"><span data-stu-id="fc933-115">Enables the **Finish** button.</span></span> <span data-ttu-id="fc933-116">Indica che si tratta dell'ultima pagina sul lato server.</span><span class="sxs-lookup"><span data-stu-id="fc933-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc933-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc933-117">Remarks</span></span>

<span data-ttu-id="fc933-118">Assicurarsi di implementare le funzioni del gestore in ogni pagina lato server per OnBack() e OnNext(), corrispondenti ai pulsanti **Indietro** e Avanti della **procedura guidata.**</span><span class="sxs-lookup"><span data-stu-id="fc933-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="fc933-119">Le funzioni OnBack() e OnNext() rispondono a **SetWizardButtons**.</span><span class="sxs-lookup"><span data-stu-id="fc933-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="fc933-120">Al momento appropriato, la funzione OnNext() chiama **SetWizardButtons** con *vbLastPage* true , che = può abilitare un **pulsante** Fine.</span><span class="sxs-lookup"><span data-stu-id="fc933-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="fc933-121">OnNext() chiama anche [**FinalNext quando**](iwebwizardhost-finalnext.md) un utente fa clic sul **pulsante** Fine.</span><span class="sxs-lookup"><span data-stu-id="fc933-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc933-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc933-122">Requirements</span></span>



| <span data-ttu-id="fc933-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc933-123">Requirement</span></span> | <span data-ttu-id="fc933-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fc933-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc933-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc933-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fc933-126">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fc933-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fc933-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc933-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fc933-128">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc933-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc933-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc933-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc933-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc933-131">Idl</span><span class="sxs-lookup"><span data-stu-id="fc933-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc933-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




