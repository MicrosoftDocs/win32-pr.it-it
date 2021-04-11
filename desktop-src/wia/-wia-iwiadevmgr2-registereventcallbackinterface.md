---
description: Registra un'applicazione in esecuzione per la notifica degli eventi di Windows Image Acquisition (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'Metodo IWiaDevMgr2:: RegisterEventCallbackInterface (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231553"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a><span data-ttu-id="255b3-103">Metodo IWiaDevMgr2:: RegisterEventCallbackInterface</span><span class="sxs-lookup"><span data-stu-id="255b3-103">IWiaDevMgr2::RegisterEventCallbackInterface method</span></span>

<span data-ttu-id="255b3-104">Registra un'applicazione in esecuzione per la notifica degli eventi di Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="255b3-104">Registers a running application for Windows Image Acquisition (WIA) 2.0 event notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="255b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="255b3-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a><span data-ttu-id="255b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="255b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="255b3-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="255b3-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="255b3-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="255b3-108">Type: **LONG**</span></span>

<span data-ttu-id="255b3-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="255b3-109">Currently unused.</span></span> <span data-ttu-id="255b3-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="255b3-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="255b3-111">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="255b3-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="255b3-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="255b3-112">Type: **BSTR**</span></span>

<span data-ttu-id="255b3-113">Specifica l'identificatore univoco di un dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="255b3-113">Specifies the unique identifier of a WIA 2.0 device.</span></span> <span data-ttu-id="255b3-114">Impostare questo parametro su **null** per registrarsi per l'evento in tutti i dispositivi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="255b3-114">Set this parameter to **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="255b3-115">*pEventGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="255b3-115">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="255b3-116">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="255b3-116">Type: \**const GUID\** _</span></span>

<span data-ttu-id="255b3-117">Specifica un puntatore all'identificatore dell'evento per cui è registrata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="255b3-117">Specifies a pointer to the event identifier that the application is registering for.</span></span> <span data-ttu-id="255b3-118">Vedere gli [identificatori di evento WIA](-wia-wia-event-identifiers.md) per gli identificatori di evento standard.</span><span class="sxs-lookup"><span data-stu-id="255b3-118">See [WIA Event Identifiers](-wia-wia-event-identifiers.md) for standard event identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="255b3-119">_pIWiaEventCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="255b3-119">_pIWiaEventCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="255b3-120">Tipo: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _</span><span class="sxs-lookup"><span data-stu-id="255b3-120">Type: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\** _</span></span>

<span data-ttu-id="255b3-121">Specifica un puntatore all'interfaccia [_ *IWiaEventCallback* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) utilizzata da WIA 2,0 per inviare la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="255b3-121">Specifies a pointer to the [_ *IWiaEventCallback*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) interface that the WIA 2.0 uses to send event notification.</span></span>

</dd> <dt>

<span data-ttu-id="255b3-122">*pEventObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="255b3-122">*pEventObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="255b3-123">Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="255b3-123">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="255b3-124">Riceve l'indirizzo di un puntatore all'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="255b3-124">Receives the address of a pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="255b3-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="255b3-125">Return value</span></span>

<span data-ttu-id="255b3-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="255b3-126">Type: **HRESULT**</span></span>

<span data-ttu-id="255b3-127">Restituisce i codici di errore COM standard o gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="255b3-127">Returns the standard COM error codes or the following.</span></span>



| <span data-ttu-id="255b3-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="255b3-128">Return code</span></span>                                                                               | <span data-ttu-id="255b3-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="255b3-129">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="255b3-130"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="255b3-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="255b3-131">Non è possibile restituire l'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="255b3-131">The [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface cannot be returned.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="255b3-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="255b3-132">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="255b3-133">L'uso dei metodi [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: RegisterEventCallbackInterface** e [**devicemanager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) dello stesso processo dopo il riavvio del servizio Still Image può causare una violazione di accesso, se le funzioni sono state usate prima dell'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="255b3-133">Using the [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface**, and [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</span></span>

 

<span data-ttu-id="255b3-134">Quando le applicazioni WIA 2,0 iniziano l'esecuzione, usano questo metodo per eseguire la registrazione in modo da ricevere gli eventi del dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="255b3-134">When WIA 2.0 applications begin executing, they use this method to register to receive hardware device events.</span></span> <span data-ttu-id="255b3-135">In questo modo si impedisce che l'applicazione venga riavviata quando si verifica un altro evento per cui è registrata.</span><span class="sxs-lookup"><span data-stu-id="255b3-135">This prevents the application from being restarted when another event for which it is registered occurs.</span></span> <span data-ttu-id="255b3-136">Quando un'applicazione chiama **IWiaDevMgr2:: RegisterEventCallbackInterface** per registrarsi per ricevere eventi WIA 2,0 da un dispositivo, gli eventi registrati vengono indirizzati al programma da WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="255b3-136">Once an application calls **IWiaDevMgr2::RegisterEventCallbackInterface** to register itself to receive WIA 2.0 events from a device, the registered events are routed to the program by WIA 2.0.</span></span>

<span data-ttu-id="255b3-137">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *pEventObject* .</span><span class="sxs-lookup"><span data-stu-id="255b3-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *pEventObject* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="255b3-138">In un'applicazione multithread, il callback della notifica degli eventi può essere presente in un thread diverso da quello che ha registrato il callback.</span><span class="sxs-lookup"><span data-stu-id="255b3-138">In a multithreaded application, the event notification callback may come in on a different thread from the one that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="255b3-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="255b3-139">Requirements</span></span>



| <span data-ttu-id="255b3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="255b3-140">Requirement</span></span> | <span data-ttu-id="255b3-141">Valore</span><span class="sxs-lookup"><span data-stu-id="255b3-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="255b3-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="255b3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="255b3-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="255b3-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="255b3-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="255b3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="255b3-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="255b3-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="255b3-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="255b3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="255b3-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="255b3-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="255b3-148">IDL</span><span class="sxs-lookup"><span data-stu-id="255b3-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="255b3-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="255b3-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
