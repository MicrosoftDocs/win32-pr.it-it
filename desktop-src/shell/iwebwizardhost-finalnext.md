---
description: Passa alla pagina della procedura guidata sul lato client che segue la pagina che ospita le pagine HTML sul lato server o termina la procedura guidata se non sono presenti altre pagine sul lato client.
title: Metodo WebWizardHost.FinalNext (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841842"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="731dd-103">Metodo WebWizardHost.FinalNext</span><span class="sxs-lookup"><span data-stu-id="731dd-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="731dd-104">Passa alla pagina della procedura guidata sul lato client che segue la pagina che ospita le pagine HTML sul lato server o termina la procedura guidata se non sono presenti altre pagine sul lato client.</span><span class="sxs-lookup"><span data-stu-id="731dd-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="731dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="731dd-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="731dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="731dd-106">Parameters</span></span>

<span data-ttu-id="731dd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="731dd-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="731dd-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="731dd-108">Remarks</span></span>

<span data-ttu-id="731dd-109">Quando la procedura guidata visualizza l'ultima pagina HTML sul  lato  server e l'utente fa clic sul pulsante Avanti o Fine, il server richiama **FinalNext** nel gestore eventi di tale pulsante.</span><span class="sxs-lookup"><span data-stu-id="731dd-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="731dd-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="731dd-110">Requirements</span></span>



| <span data-ttu-id="731dd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="731dd-111">Requirement</span></span> | <span data-ttu-id="731dd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="731dd-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="731dd-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="731dd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="731dd-114">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="731dd-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="731dd-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="731dd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="731dd-116">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="731dd-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="731dd-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="731dd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="731dd-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="731dd-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="731dd-119">Idl</span><span class="sxs-lookup"><span data-stu-id="731dd-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="731dd-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="731dd-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




