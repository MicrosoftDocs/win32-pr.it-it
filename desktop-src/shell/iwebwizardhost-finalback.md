---
description: Passa alla pagina lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.
title: Metodo WebWizardHost. FinalBack (shldisp. h)
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
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882485"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="347f1-103">WebWizardHost. FinalBack, metodo</span><span class="sxs-lookup"><span data-stu-id="347f1-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="347f1-104">Passa alla pagina lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.</span><span class="sxs-lookup"><span data-stu-id="347f1-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="347f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="347f1-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="347f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="347f1-106">Parameters</span></span>

<span data-ttu-id="347f1-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="347f1-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="347f1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="347f1-108">Remarks</span></span>

<span data-ttu-id="347f1-109">Quando la procedura guidata Visualizza la prima pagina sul lato server e l'utente fa clic sul pulsante **indietro** , il server richiama **FinalBack** quando riceve una notifica dell'evento da parte del gestore eventi del client.</span><span class="sxs-lookup"><span data-stu-id="347f1-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="347f1-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="347f1-110">Requirements</span></span>



| <span data-ttu-id="347f1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="347f1-111">Requirement</span></span> | <span data-ttu-id="347f1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="347f1-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="347f1-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="347f1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="347f1-114">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="347f1-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="347f1-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="347f1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="347f1-116">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="347f1-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="347f1-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="347f1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="347f1-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="347f1-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="347f1-119">IDL</span><span class="sxs-lookup"><span data-stu-id="347f1-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="347f1-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="347f1-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




