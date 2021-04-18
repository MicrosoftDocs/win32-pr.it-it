---
description: Le \_ costanti LINEINITIALIZEEXOPTION specificano il meccanismo di notifica degli eventi da usare per l'inizializzazione di una sessione.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Costanti LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331029"
---
# <a name="lineinitializeexoption_-constants"></a><span data-ttu-id="5c027-103">\_Costanti LINEINITIALIZEEXOPTION</span><span class="sxs-lookup"><span data-stu-id="5c027-103">LINEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="5c027-104">Le **costanti \_ LINEINITIALIZEEXOPTION** specificano il meccanismo di notifica degli eventi da usare per l'inizializzazione di una sessione.</span><span class="sxs-lookup"><span data-stu-id="5c027-104">The **LINEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="5c027-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**\_CALLHUBTRACKING LINEINITIALIZEEXOPTION**</span><span class="sxs-lookup"><span data-stu-id="5c027-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5c027-106">L'applicazione desidera usare il meccanismo di notifica degli eventi di rilevamento dell'hub chiamate.</span><span class="sxs-lookup"><span data-stu-id="5c027-106">The application desires to use the call hub tracking event notification mechanism.</span></span> <span data-ttu-id="5c027-107">Questa costante viene esposta solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5c027-107">This constant is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c027-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**\_USECOMPLETIONPORT LINEINITIALIZEEXOPTION**</span><span class="sxs-lookup"><span data-stu-id="5c027-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5c027-109">L'applicazione desidera utilizzare il meccanismo di notifica degli eventi della porta di completamento.</span><span class="sxs-lookup"><span data-stu-id="5c027-109">The application desires to use the Completion Port event notification mechanism.</span></span> <span data-ttu-id="5c027-110">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5c027-110">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c027-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**\_USEEVENT LINEINITIALIZEEXOPTION**</span><span class="sxs-lookup"><span data-stu-id="5c027-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5c027-112">L'applicazione desidera utilizzare il meccanismo di notifica degli eventi del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="5c027-112">The application desires to use the Event Handle event notification mechanism.</span></span> <span data-ttu-id="5c027-113">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5c027-113">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5c027-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**\_USEHIDDENWINDOW LINEINITIALIZEEXOPTION**</span><span class="sxs-lookup"><span data-stu-id="5c027-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5c027-115">L'applicazione desidera utilizzare il meccanismo di notifica degli eventi della finestra nascosta.</span><span class="sxs-lookup"><span data-stu-id="5c027-115">The application desires to use the Hidden Window event notification mechanism.</span></span> <span data-ttu-id="5c027-116">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5c027-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c027-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c027-117">Remarks</span></span>

<span data-ttu-id="5c027-118">Per ulteriori informazioni sul funzionamento di queste opzioni, vedere [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="5c027-118">See [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c027-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c027-119">Requirements</span></span>



| <span data-ttu-id="5c027-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c027-120">Requirement</span></span> | <span data-ttu-id="5c027-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5c027-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5c027-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5c027-122">TAPI version</span></span><br/> | <span data-ttu-id="5c027-123">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5c027-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5c027-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c027-124">Header</span></span><br/>       | <dl> <span data-ttu-id="5c027-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c027-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




