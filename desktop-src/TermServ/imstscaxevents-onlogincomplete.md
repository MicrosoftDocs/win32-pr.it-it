---
title: Metodo IMsTscAxEvents OnLoginComplete
description: Chiamato quando il controllo client ha effettuato l'accesso a un server di host sessione Desktop remoto (host sessione Desktop remoto), dopo la visualizzazione della finestra di dialogo di accesso di Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnLoginComplete
- Metodo OnLoginComplete Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518057"
---
# <a name="imstscaxeventsonlogincomplete-method"></a><span data-ttu-id="ffefe-106">Metodo IMsTscAxEvents:: OnLoginComplete</span><span class="sxs-lookup"><span data-stu-id="ffefe-106">IMsTscAxEvents::OnLoginComplete method</span></span>

<span data-ttu-id="ffefe-107">Chiamato quando il controllo client ha effettuato l'accesso a un server di host sessione Desktop remoto (host sessione Desktop remoto), dopo la visualizzazione della finestra di dialogo di accesso di Windows.</span><span class="sxs-lookup"><span data-stu-id="ffefe-107">Called when the client control has successfully logged on to a Remote Desktop Session Host (RD Session Host) server, following the display of the Windows Logon dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffefe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffefe-108">Syntax</span></span>


```C++
void OnLoginComplete();
```



## <a name="parameters"></a><span data-ttu-id="ffefe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffefe-109">Parameters</span></span>

<span data-ttu-id="ffefe-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ffefe-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ffefe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffefe-111">Return value</span></span>

<span data-ttu-id="ffefe-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ffefe-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffefe-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffefe-113">Remarks</span></span>

<span data-ttu-id="ffefe-114">Implementare questo metodo nel sink di evento per ricevere la notifica che il controllo ha completato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="ffefe-114">Implement this method in your event sink to receive notification that the control has completed logon.</span></span>

## <a name="examples"></a><span data-ttu-id="ffefe-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="ffefe-115">Examples</span></span>

<span data-ttu-id="ffefe-116">Nell'esempio seguente viene illustrato come gestire questo evento utilizzando Visual Basic codice di scripting.</span><span class="sxs-lookup"><span data-stu-id="ffefe-116">The following example shows how to handle this event by using Visual Basic Scripting code.</span></span> <span data-ttu-id="ffefe-117">Il presupposto in questo esempio è che l'oggetto controllo è denominato "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="ffefe-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="ffefe-118">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ffefe-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a><span data-ttu-id="ffefe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffefe-119">Requirements</span></span>



| <span data-ttu-id="ffefe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffefe-120">Requirement</span></span> | <span data-ttu-id="ffefe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ffefe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffefe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffefe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ffefe-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffefe-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ffefe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffefe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ffefe-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffefe-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ffefe-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ffefe-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="ffefe-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffefe-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ffefe-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ffefe-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffefe-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffefe-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ffefe-130">IID</span><span class="sxs-lookup"><span data-stu-id="ffefe-130">IID</span></span><br/>                      | <span data-ttu-id="ffefe-131">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="ffefe-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ffefe-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffefe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffefe-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="ffefe-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





