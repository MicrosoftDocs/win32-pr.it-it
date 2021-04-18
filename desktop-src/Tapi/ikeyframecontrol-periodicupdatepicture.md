---
description: Il metodo PeriodicUpdatePicture viene chiamato da un'applicazione per configurare un timer nel flusso che richiederà periodicamente gli aggiornamenti delle immagini. Gli aggiornamenti delle immagini provocano un utilizzo elevato della larghezza di banda, quindi questo metodo viene normalmente usato al posto di UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: Metodo IKeyFrameControl::P eriodicUpdatePicture (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324762"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a><span data-ttu-id="a3c1a-104">IKeyFrameControl::P metodo eriodicUpdatePicture</span><span class="sxs-lookup"><span data-stu-id="a3c1a-104">IKeyFrameControl::PeriodicUpdatePicture method</span></span>

<span data-ttu-id="a3c1a-105">\[**PeriodicUpdatePicture** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-105">\[**PeriodicUpdatePicture** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a3c1a-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a3c1a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a3c1a-107">Il metodo **PeriodicUpdatePicture** viene chiamato da un'applicazione per configurare un timer nel flusso che richiederà periodicamente gli aggiornamenti delle immagini.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-107">The **PeriodicUpdatePicture** method is called by an application to configure a timer in the stream that will ask for picture updates periodically.</span></span> <span data-ttu-id="a3c1a-108">Gli aggiornamenti delle immagini provocano un utilizzo elevato della larghezza di banda, quindi questo metodo viene normalmente usato al posto di [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span><span class="sxs-lookup"><span data-stu-id="a3c1a-108">Picture updates cause high bandwidth usage, so this method will normally be used instead of [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span></span>

<span data-ttu-id="a3c1a-109">Se il metodo viene chiamato quando il flusso è attivo, il timer verrà avviato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-109">If the method is called when the stream is active, the timer will start immediately.</span></span> <span data-ttu-id="a3c1a-110">Se il flusso non è attivo, il timer viene avviato quando il flusso entra nello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-110">If the stream is not active, the timer will be started when the stream enters the active state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c1a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3c1a-111">Syntax</span></span>


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a><span data-ttu-id="a3c1a-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3c1a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c1a-113">*fEnable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3c1a-113">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3c1a-114">**True** Abilita il timer.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-114">**TRUE** enables the timer.</span></span> <span data-ttu-id="a3c1a-115">**False** lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-115">**FALSE** disables it.</span></span>

</dd> <dt>

<span data-ttu-id="a3c1a-116">*dwInterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3c1a-116">*dwInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3c1a-117">Intervallo del timer, in secondi.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-117">The interval for the timer, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c1a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3c1a-118">Return value</span></span>

<span data-ttu-id="a3c1a-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-119">This method can return one of these values.</span></span>



| <span data-ttu-id="a3c1a-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a3c1a-120">Return code</span></span>                                                                            | <span data-ttu-id="a3c1a-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3c1a-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a3c1a-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3c1a-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a3c1a-123">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-123">Method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="a3c1a-124"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="a3c1a-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a3c1a-125">Non riuscito per motivi imprevisti.</span><span class="sxs-lookup"><span data-stu-id="a3c1a-125">Failed for unexpected reasons.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a3c1a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3c1a-126">Requirements</span></span>



| <span data-ttu-id="a3c1a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3c1a-127">Requirement</span></span> | <span data-ttu-id="a3c1a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a3c1a-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c1a-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a3c1a-129">TAPI version</span></span><br/> | <span data-ttu-id="a3c1a-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a3c1a-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a3c1a-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3c1a-131">Header</span></span><br/>       | <dl> <span data-ttu-id="a3c1a-132"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c1a-132"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="a3c1a-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3c1a-133">Library</span></span><br/>      | <dl> <span data-ttu-id="a3c1a-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3c1a-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a3c1a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a3c1a-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="a3c1a-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3c1a-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a3c1a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3c1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3c1a-138">MSP H323</span><span class="sxs-lookup"><span data-stu-id="a3c1a-138">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

 




