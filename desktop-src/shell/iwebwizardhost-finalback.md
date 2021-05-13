---
description: Passa alla pagina sul lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.
title: Metodo WebWizardHost.FinalBack (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841872"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="9f546-103">Metodo WebWizardHost.FinalBack</span><span class="sxs-lookup"><span data-stu-id="9f546-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="9f546-104">Passa alla pagina sul lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.</span><span class="sxs-lookup"><span data-stu-id="9f546-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f546-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f546-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="9f546-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f546-106">Parameters</span></span>

<span data-ttu-id="9f546-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9f546-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f546-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f546-108">Remarks</span></span>

<span data-ttu-id="9f546-109">Quando la procedura guidata visualizza la prima pagina  sul lato server e l'utente fa clic sul pulsante Indietro, il server richiama **FinalBack** quando viene notificata tale evento dal gestore eventi del client.</span><span class="sxs-lookup"><span data-stu-id="9f546-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f546-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f546-110">Requirements</span></span>



| <span data-ttu-id="9f546-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f546-111">Requirement</span></span> | <span data-ttu-id="9f546-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9f546-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f546-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f546-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9f546-114">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9f546-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9f546-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f546-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9f546-116">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f546-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9f546-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f546-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f546-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="9f546-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f546-119">Idl</span><span class="sxs-lookup"><span data-stu-id="9f546-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f546-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f546-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




