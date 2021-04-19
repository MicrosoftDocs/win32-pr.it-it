---
description: L'interfaccia ITParticipantControl viene implementata da IPConf MSP.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interfaccia ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328731"
---
# <a name="itparticipantcontrol-interface"></a><span data-ttu-id="69d8d-103">Interfaccia ITParticipantControl</span><span class="sxs-lookup"><span data-stu-id="69d8d-103">ITParticipantControl interface</span></span>

<span data-ttu-id="69d8d-104">\[**ITParticipantControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="69d8d-104">\[**ITParticipantControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="69d8d-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="69d8d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="69d8d-106">L'interfaccia **ITParticipantControl** viene implementata da IPConf msp.</span><span class="sxs-lookup"><span data-stu-id="69d8d-106">The **ITParticipantControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="69d8d-107">Questa interfaccia viene esposta nell'oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="69d8d-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="69d8d-108">Questa interfaccia consente a un'applicazione di recuperare i puntatori ai partecipanti in una conferenza.</span><span class="sxs-lookup"><span data-stu-id="69d8d-108">This interface allows an application to retrieve pointers to the participants in a conference.</span></span> <span data-ttu-id="69d8d-109">L'interfaccia **ITParticipantControl** viene creata chiamando **QueryInterface** in [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="69d8d-109">The **ITParticipantControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="69d8d-110">Membri</span><span class="sxs-lookup"><span data-stu-id="69d8d-110">Members</span></span>

<span data-ttu-id="69d8d-111">L'interfaccia **ITParticipantControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="69d8d-111">The **ITParticipantControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="69d8d-112">**ITParticipantControl** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="69d8d-112">**ITParticipantControl** also has these types of members:</span></span>

-   [<span data-ttu-id="69d8d-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="69d8d-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="69d8d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="69d8d-114">Methods</span></span>

<span data-ttu-id="69d8d-115">L'interfaccia **ITParticipantControl** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="69d8d-115">The **ITParticipantControl** interface has these methods.</span></span>



| <span data-ttu-id="69d8d-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="69d8d-116">Method</span></span>                                                                      | <span data-ttu-id="69d8d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69d8d-117">Description</span></span>                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d8d-118">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="69d8d-118">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md) | <span data-ttu-id="69d8d-119">Enumera i partecipanti attualmente associati alla conferenza.</span><span class="sxs-lookup"><span data-stu-id="69d8d-119">Enumerates participants currently involved in the conference.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="69d8d-120">**Ricevi \_ i partecipanti**</span><span class="sxs-lookup"><span data-stu-id="69d8d-120">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)          | <span data-ttu-id="69d8d-121">Crea una raccolta di partecipanti associati alla conferenza corrente.</span><span class="sxs-lookup"><span data-stu-id="69d8d-121">Creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="69d8d-122">Fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="69d8d-122">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="69d8d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69d8d-123">Requirements</span></span>



| <span data-ttu-id="69d8d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d8d-124">Requirement</span></span> | <span data-ttu-id="69d8d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="69d8d-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69d8d-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="69d8d-126">TAPI version</span></span><br/> | <span data-ttu-id="69d8d-127">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="69d8d-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="69d8d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69d8d-128">Header</span></span><br/>       | <dl> <span data-ttu-id="69d8d-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d8d-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="69d8d-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="69d8d-130">Library</span></span><br/>      | <dl> <span data-ttu-id="69d8d-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69d8d-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="69d8d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="69d8d-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="69d8d-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69d8d-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

