---
description: Passa alla pagina della procedura guidata lato client che segue la pagina che ospita le pagine HTML sul lato server oppure termina la procedura guidata se non sono presenti altre pagine lato client.
title: Metodo WebWizardHost. FinalNext (shldisp. h)
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
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232493"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="d92ac-103">WebWizardHost. FinalNext, metodo</span><span class="sxs-lookup"><span data-stu-id="d92ac-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="d92ac-104">Passa alla pagina della procedura guidata lato client che segue la pagina che ospita le pagine HTML sul lato server oppure termina la procedura guidata se non sono presenti altre pagine lato client.</span><span class="sxs-lookup"><span data-stu-id="d92ac-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d92ac-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="d92ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d92ac-106">Parameters</span></span>

<span data-ttu-id="d92ac-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d92ac-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92ac-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d92ac-108">Remarks</span></span>

<span data-ttu-id="d92ac-109">Quando la procedura guidata Visualizza l'ultima pagina HTML sul lato server e l'utente fa clic sul pulsante **Avanti** o **fine** , il server richiama **FinalNext** nel gestore eventi del pulsante.</span><span class="sxs-lookup"><span data-stu-id="d92ac-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92ac-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d92ac-110">Requirements</span></span>



| <span data-ttu-id="d92ac-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d92ac-111">Requirement</span></span> | <span data-ttu-id="d92ac-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d92ac-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d92ac-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d92ac-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d92ac-114">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d92ac-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d92ac-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d92ac-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d92ac-116">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d92ac-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d92ac-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d92ac-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d92ac-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d92ac-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d92ac-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d92ac-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d92ac-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d92ac-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




