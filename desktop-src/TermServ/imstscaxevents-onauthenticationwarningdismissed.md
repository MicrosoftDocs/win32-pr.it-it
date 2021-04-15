---
title: Metodo IMsTscAxEvents OnAuthenticationWarningDismissed
description: Viene chiamato dopo che un controllo ActiveX Visualizza una finestra di dialogo di autenticazione (ad esempio, la finestra di dialogo errore certificato).
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAuthenticationWarningDismissed
- Metodo OnAuthenticationWarningDismissed Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400585"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a><span data-ttu-id="12f28-106">Metodo IMsTscAxEvents:: OnAuthenticationWarningDismissed</span><span class="sxs-lookup"><span data-stu-id="12f28-106">IMsTscAxEvents::OnAuthenticationWarningDismissed method</span></span>

<span data-ttu-id="12f28-107">Viene chiamato dopo che un controllo ActiveX Visualizza una finestra di dialogo di autenticazione (ad esempio, la finestra di dialogo errore certificato).</span><span class="sxs-lookup"><span data-stu-id="12f28-107">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="12f28-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12f28-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a><span data-ttu-id="12f28-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="12f28-109">Parameters</span></span>

<span data-ttu-id="12f28-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="12f28-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12f28-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12f28-111">Return value</span></span>

<span data-ttu-id="12f28-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="12f28-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12f28-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="12f28-113">Remarks</span></span>

<span data-ttu-id="12f28-114">Se necessario, è possibile usare la proprietà [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) dell'interfaccia [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) per ripristinare gli elementi padre che potrebbero essere stati eseguiti nel metodo [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) .</span><span class="sxs-lookup"><span data-stu-id="12f28-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to revert any parenting that may have been done in the [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) method.</span></span>

<span data-ttu-id="12f28-115">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="12f28-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12f28-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12f28-116">Requirements</span></span>



| <span data-ttu-id="12f28-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f28-117">Requirement</span></span> | <span data-ttu-id="12f28-118">Valore</span><span class="sxs-lookup"><span data-stu-id="12f28-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12f28-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12f28-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12f28-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12f28-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="12f28-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12f28-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12f28-122">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="12f28-122">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="12f28-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="12f28-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="12f28-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f28-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="12f28-125">DLL</span><span class="sxs-lookup"><span data-stu-id="12f28-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12f28-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f28-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="12f28-127">IID</span><span class="sxs-lookup"><span data-stu-id="12f28-127">IID</span></span><br/>                      | <span data-ttu-id="12f28-128">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="12f28-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="12f28-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12f28-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f28-130">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="12f28-130">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="12f28-131">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="12f28-131">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="12f28-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="12f28-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





