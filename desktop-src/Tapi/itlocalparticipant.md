---
description: L'interfaccia ITLocalParticipant viene esposta nell'oggetto flusso quando IPConf MSP supporta la chiamata.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interfaccia ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330369"
---
# <a name="itlocalparticipant-interface"></a><span data-ttu-id="c696b-103">Interfaccia ITLocalParticipant</span><span class="sxs-lookup"><span data-stu-id="c696b-103">ITLocalParticipant interface</span></span>

<span data-ttu-id="c696b-104">L'interfaccia **ITLocalParticipant** viene esposta nell'oggetto flusso quando IPConf msp supporta la chiamata.</span><span class="sxs-lookup"><span data-stu-id="c696b-104">The **ITLocalParticipant** interface is exposed on the stream object when the IPConf MSP supports the call.</span></span> <span data-ttu-id="c696b-105">Il MSP implementa i metodi che consentono a un'applicazione di ottenere e impostare informazioni sul partecipante.</span><span class="sxs-lookup"><span data-stu-id="c696b-105">The MSP implements methods that allow an application to get and set participant information.</span></span> <span data-ttu-id="c696b-106">L'interfaccia **ITLocalParticipant** viene creata chiamando **QueryInterface** in [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="c696b-106">The **ITLocalParticipant** interface is created by calling **QueryInterface** on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>

## <a name="members"></a><span data-ttu-id="c696b-107">Membri</span><span class="sxs-lookup"><span data-stu-id="c696b-107">Members</span></span>

<span data-ttu-id="c696b-108">L'interfaccia **ITLocalParticipant** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c696b-108">The **ITLocalParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c696b-109">**ITLocalParticipant** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c696b-109">**ITLocalParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="c696b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c696b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c696b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c696b-111">Methods</span></span>

<span data-ttu-id="c696b-112">L'interfaccia **ITLocalParticipant** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c696b-112">The **ITLocalParticipant** interface has these methods.</span></span>



| <span data-ttu-id="c696b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="c696b-113">Method</span></span>                                                                                     | <span data-ttu-id="c696b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c696b-114">Description</span></span>                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="c696b-115">**ottenere \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="c696b-115">**get\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-get-localparticipanttypedinfo.md) | <span data-ttu-id="c696b-116">Ottiene le informazioni sul partecipante, ad esempio il nome della posta elettronica o la posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="c696b-116">Gets participant information, such as e-mail name or geographical location.</span></span><br/> |
| [<span data-ttu-id="c696b-117">**Inserisci \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="c696b-117">**put\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-put-localparticipanttypedinfo.md) | <span data-ttu-id="c696b-118">Imposta le informazioni sul partecipante.</span><span class="sxs-lookup"><span data-stu-id="c696b-118">Sets participant information.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="c696b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c696b-119">Requirements</span></span>



| <span data-ttu-id="c696b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c696b-120">Requirement</span></span> | <span data-ttu-id="c696b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c696b-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c696b-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c696b-122">TAPI version</span></span><br/> | <span data-ttu-id="c696b-123">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c696b-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c696b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c696b-124">Header</span></span><br/>       | <dl> <span data-ttu-id="c696b-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="c696b-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="c696b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c696b-126">Library</span></span><br/>      | <dl> <span data-ttu-id="c696b-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c696b-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c696b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c696b-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="c696b-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c696b-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c696b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c696b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c696b-131">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="c696b-131">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

