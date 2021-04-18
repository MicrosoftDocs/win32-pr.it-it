---
description: Le \_ costanti PHONEINITIALIZEEXOPTION specificano il meccanismo di notifica degli eventi da usare per l'inizializzazione di una sessione.
ms.assetid: 7d8b122d-bebe-4904-abc8-d680b0899e25
title: Costanti PHONEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023f6801f65910bedf7d2637079694b4c6b6d85e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333942"
---
# <a name="phoneinitializeexoption_-constants"></a><span data-ttu-id="dadf3-103">\_Costanti PHONEINITIALIZEEXOPTION</span><span class="sxs-lookup"><span data-stu-id="dadf3-103">PHONEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="dadf3-104">Le **costanti \_ PHONEINITIALIZEEXOPTION** specificano il meccanismo di notifica degli eventi da usare per l'inizializzazione di una sessione.</span><span class="sxs-lookup"><span data-stu-id="dadf3-104">The **PHONEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="dadf3-105"><span id="PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="phoneinitializeexoption_usecompletionport"></span>**\_USECOMPLETIONPORT PHONEINITIALIZEEXOPTION**</span><span class="sxs-lookup"><span data-stu-id="dadf3-105"><span id="PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="phoneinitializeexoption_usecompletionport"></span>**PHONEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dadf3-106">L'applicazione desidera utilizzare il meccanismo di notifica degli eventi della porta di completamento.</span><span class="sxs-lookup"><span data-stu-id="dadf3-106">The application desires to use the Completion Port event notification mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dadf3-107"><span id="PHONEINITIALIZEEXOPTION_USEEVENT"></span><span id="phoneinitializeexoption_useevent"></span>**\_USEEVENT PHONEINITIALIZEEXOPTION**</span><span class="sxs-lookup"><span data-stu-id="dadf3-107"><span id="PHONEINITIALIZEEXOPTION_USEEVENT"></span><span id="phoneinitializeexoption_useevent"></span>**PHONEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dadf3-108">L'applicazione desidera utilizzare il meccanismo di notifica degli eventi del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="dadf3-108">The application desires to use the Event Handle event notification mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dadf3-109"><span id="PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="phoneinitializeexoption_usehiddenwindow"></span>**\_USEHIDDENWINDOW PHONEINITIALIZEEXOPTION**</span><span class="sxs-lookup"><span data-stu-id="dadf3-109"><span id="PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="phoneinitializeexoption_usehiddenwindow"></span>**PHONEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dadf3-110">L'applicazione desidera utilizzare il meccanismo di notifica degli eventi della finestra nascosta.</span><span class="sxs-lookup"><span data-stu-id="dadf3-110">The application desires to use the Hidden Window event notification mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dadf3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="dadf3-111">Remarks</span></span>

<span data-ttu-id="dadf3-112">Per ulteriori informazioni sul funzionamento di queste opzioni, vedere [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="dadf3-112">See [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="dadf3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dadf3-113">Requirements</span></span>



| <span data-ttu-id="dadf3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dadf3-114">Requirement</span></span> | <span data-ttu-id="dadf3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="dadf3-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dadf3-116">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="dadf3-116">TAPI version</span></span><br/> | <span data-ttu-id="dadf3-117">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dadf3-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dadf3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dadf3-118">Header</span></span><br/>       | <dl> <span data-ttu-id="dadf3-119"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dadf3-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




