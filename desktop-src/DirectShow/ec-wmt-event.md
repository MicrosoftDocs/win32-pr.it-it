---
description: Inviato dal filtro di lettura ASF WM quando legge i file ASF protetti da Digital Rights Management (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325491"
---
# <a name="ec_wmt_event-dshowh"></a><span data-ttu-id="2ddca-103">EC_WMT_EVENT (dshow. h)</span><span class="sxs-lookup"><span data-stu-id="2ddca-103">EC_WMT_EVENT (Dshow.h)</span></span>

<span data-ttu-id="2ddca-104">Inviato dal filtro di [lettura ASF WM](wm-asf-reader-filter.md) quando legge i file ASF protetti da Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="2ddca-104">Sent by the [WM ASF Reader](wm-asf-reader-filter.md) filter when it reads ASF files protected by digital rights management (DRM).</span></span>

## <a name="parameters"></a><span data-ttu-id="2ddca-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ddca-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddca-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2ddca-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2ddca-107">Uno dei valori di **\_ stato di WMT** seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ddca-107">One of the following **WMT\_STATUS** values:</span></span>



| <span data-ttu-id="2ddca-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2ddca-108">Value</span></span>                         | <span data-ttu-id="2ddca-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ddca-109">Description</span></span>                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddca-110">\_licenza di acquisizione WMT \_</span><span class="sxs-lookup"><span data-stu-id="2ddca-110">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="2ddca-111">Inviato quando il componente DRM ha completato il processo di acquisizione della licenza, con esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="2ddca-111">Sent when the DRM component has completed the license acquisition process, either successfully or unsuccessfully.</span></span> |
| <span data-ttu-id="2ddca-112">WMT di \_ personalizzazione</span><span class="sxs-lookup"><span data-stu-id="2ddca-112">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="2ddca-113">Il processo di aggiornamento della sicurezza è stato completato correttamente o senza esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2ddca-113">The security upgrade process has completed, either successfully or unsuccessfully.</span></span>                                |
| <span data-ttu-id="2ddca-114">WMT \_ richiede l' \_ individualizzazione</span><span class="sxs-lookup"><span data-stu-id="2ddca-114">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="2ddca-115">Il file richiede che un'applicazione riceva un aggiornamento della sicurezza prima di eseguire l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="2ddca-115">The file requires that an application receive a security upgrade before performing the requested action.</span></span>          |
| <span data-ttu-id="2ddca-116">\_nessun \_ diritto di WMT</span><span class="sxs-lookup"><span data-stu-id="2ddca-116">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="2ddca-117">L'applicazione non dispone dei diritti necessari per eseguire l'azione richiesta su un file protetto da DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="2ddca-117">The application has no rights to perform he requested action on a file protected by DRM version 1.</span></span>                |
| <span data-ttu-id="2ddca-118">WMT \_ No \_ Rights \_</span><span class="sxs-lookup"><span data-stu-id="2ddca-118">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="2ddca-119">L'applicazione non dispone dei diritti necessari per eseguire l'azione richiesta su un file protetto da DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="2ddca-119">The application has no rights to perform he requested action on a file protected by DRM version 7.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="2ddca-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2ddca-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2ddca-121">Puntatore a una struttura di [**\_ dati dell' \_ evento \_ am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) che contiene informazioni sull'evento o **null**.</span><span class="sxs-lookup"><span data-stu-id="2ddca-121">Pointer to an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) structure that contains information about the event, or **NULL**.</span></span> <span data-ttu-id="2ddca-122">Il membro **pData** di questa struttura punta a dati aggiuntivi il cui tipo dipende dal valore di **lParam1**, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2ddca-122">The **pData** member of this structure points to additional data, whose type depends on the value of **lParam1**, as shown in the following table.</span></span>



| <span data-ttu-id="2ddca-123">lParam1</span><span class="sxs-lookup"><span data-stu-id="2ddca-123">lParam1</span></span>                       | <span data-ttu-id="2ddca-124">\_ \_ Dati evento WMT \_ . pData</span><span class="sxs-lookup"><span data-stu-id="2ddca-124">AM\_WMT\_EVENT\_DATA.pData</span></span>                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddca-125">\_licenza di acquisizione WMT \_</span><span class="sxs-lookup"><span data-stu-id="2ddca-125">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="2ddca-126">Puntatore a una struttura di [**\_ dati di \_ licenza \_ WM Get**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="2ddca-126">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span> <span data-ttu-id="2ddca-127">Questa struttura è documentata in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="2ddca-127">This structure is documented in the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="2ddca-128">WMT di \_ personalizzazione</span><span class="sxs-lookup"><span data-stu-id="2ddca-128">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="2ddca-129">Puntatore a una struttura di [**\_ \_ stato di personalizzazione WM**](/windows/desktop/wmformat/wm-individualize-status) .</span><span class="sxs-lookup"><span data-stu-id="2ddca-129">Pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](/windows/desktop/wmformat/wm-individualize-status) structure.</span></span>                                                        |
| <span data-ttu-id="2ddca-130">WMT \_ richiede l' \_ individualizzazione</span><span class="sxs-lookup"><span data-stu-id="2ddca-130">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="2ddca-131">**Valore null**.</span><span class="sxs-lookup"><span data-stu-id="2ddca-131">**NULL**.</span></span>                                                                                                                                        |
| <span data-ttu-id="2ddca-132">\_nessun \_ diritto di WMT</span><span class="sxs-lookup"><span data-stu-id="2ddca-132">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="2ddca-133">Puntatore a una stringa di caratteri wide contenente un URL della richiesta di verifica.</span><span class="sxs-lookup"><span data-stu-id="2ddca-133">Pointer to a wide-character string containing a challenge URL.</span></span>                                                                                   |
| <span data-ttu-id="2ddca-134">WMT \_ No \_ Rights \_</span><span class="sxs-lookup"><span data-stu-id="2ddca-134">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="2ddca-135">Puntatore a una struttura di [**\_ dati di \_ licenza \_ WM Get**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="2ddca-135">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span>                                                               |



 

<span data-ttu-id="2ddca-136">Il valore di *lParam2* potrebbe essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2ddca-136">The value of *lParam2* might be **NULL**.</span></span> <span data-ttu-id="2ddca-137">Verificare il valore prima di dereferenziare il puntatore.</span><span class="sxs-lookup"><span data-stu-id="2ddca-137">Check the value before dereferencing the pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ddca-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ddca-138">Remarks</span></span>

<span data-ttu-id="2ddca-139">Per ulteriori informazioni sull'abilitazione della riproduzione di file protetti da DRM, vedere la documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="2ddca-139">See the Windows Media Format SDK documentation for more information on enabling playback of DRM-protected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddca-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ddca-140">Requirements</span></span>



| <span data-ttu-id="2ddca-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddca-141">Requirement</span></span> | <span data-ttu-id="2ddca-142">Valore</span><span class="sxs-lookup"><span data-stu-id="2ddca-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddca-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ddca-143">Header</span></span><br/> | <dl> <span data-ttu-id="2ddca-144"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddca-144"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddca-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ddca-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddca-146">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="2ddca-146">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2ddca-147">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="2ddca-147">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

