---
title: Metodo IMsTscAxEvents OnAuthenticationWarningDisplayed
description: Chiamato prima che un controllo ActiveX visualizzi una finestra di dialogo di autenticazione (ad esempio, la finestra di dialogo errore certificato).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAuthenticationWarningDisplayed
- Metodo OnAuthenticationWarningDisplayed Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119634"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a><span data-ttu-id="ecc71-106">Metodo IMsTscAxEvents:: OnAuthenticationWarningDisplayed</span><span class="sxs-lookup"><span data-stu-id="ecc71-106">IMsTscAxEvents::OnAuthenticationWarningDisplayed method</span></span>

<span data-ttu-id="ecc71-107">Chiamato prima che un controllo ActiveX visualizzi una finestra di dialogo di autenticazione (ad esempio, la finestra di dialogo errore certificato).</span><span class="sxs-lookup"><span data-stu-id="ecc71-107">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc71-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecc71-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a><span data-ttu-id="ecc71-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecc71-109">Parameters</span></span>

<span data-ttu-id="ecc71-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ecc71-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ecc71-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecc71-111">Return value</span></span>

<span data-ttu-id="ecc71-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ecc71-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecc71-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecc71-113">Remarks</span></span>

<span data-ttu-id="ecc71-114">Se necessario, è possibile usare la proprietà [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) dell'interfaccia [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) per assicurarsi che la finestra di dialogo di autenticazione modale da visualizzare venga impostata come elemento padre da una finestra specificata (potrebbe essere necessario impedire agli utenti di usare altre finestre di dialogo durante la visualizzazione della finestra di dialogo di autenticazione).</span><span class="sxs-lookup"><span data-stu-id="ecc71-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to ensure that the modal authentication dialog to be displayed will be parented by a specified window (this may be necessary to prevent users from using other dialog boxes while the authentication dialog box is displayed).</span></span> <span data-ttu-id="ecc71-115">Per impostazione predefinita, l'elemento padre è la finestra del controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ecc71-115">By default, the parent is the ActiveX control window.</span></span>

<span data-ttu-id="ecc71-116">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ecc71-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc71-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecc71-117">Requirements</span></span>



| <span data-ttu-id="ecc71-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecc71-118">Requirement</span></span> | <span data-ttu-id="ecc71-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ecc71-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc71-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecc71-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc71-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecc71-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ecc71-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecc71-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc71-123">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="ecc71-123">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="ecc71-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ecc71-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ecc71-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecc71-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ecc71-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ecc71-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecc71-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecc71-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ecc71-128">IID</span><span class="sxs-lookup"><span data-stu-id="ecc71-128">IID</span></span><br/>                      | <span data-ttu-id="ecc71-129">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="ecc71-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ecc71-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecc71-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc71-131">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="ecc71-131">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="ecc71-132">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="ecc71-132">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="ecc71-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="ecc71-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





