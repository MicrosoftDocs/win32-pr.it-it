---
title: Costanti WINBIO_POOL (tipi WinBio \_ . h)
description: Consente di specificare il tipo di pool di unità biometriche da usare nella sessione.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519024"
---
# <a name="winbio_pool-constants"></a><span data-ttu-id="e139a-103">\_Costanti pool WINBIO</span><span class="sxs-lookup"><span data-stu-id="e139a-103">WINBIO\_POOL Constants</span></span>

<span data-ttu-id="e139a-104">Nella funzione [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) è possibile usare le costanti seguenti per specificare il tipo di pool di unità biometriche da usare nella sessione.</span><span class="sxs-lookup"><span data-stu-id="e139a-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify the type of biometric unit pool to be used in the session.</span></span>



| <span data-ttu-id="e139a-105">Costante</span><span class="sxs-lookup"><span data-stu-id="e139a-105">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="e139a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e139a-106">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="e139a-107"><dt>**\_pool WINBIO \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="e139a-107"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="e139a-108">Il tipo di pool è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e139a-108">The pool type is unknown.</span></span><br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="e139a-109"><dt>**\_sistema pool \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="e139a-109"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>             | <span data-ttu-id="e139a-110">Specifica una raccolta condivisa di unità biometriche gestite dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="e139a-110">Specifies a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="e139a-111"><dt>**\_pool WINBIO \_ privato**</dt></span><span class="sxs-lookup"><span data-stu-id="e139a-111"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl>          | <span data-ttu-id="e139a-112">Specifica una raccolta di unità biometriche gestite dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="e139a-112">Specifies a collection of biometric units that are managed by the caller.</span></span><br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <span data-ttu-id="e139a-113"><dt>**POOL WINBIO non \_ \_ assegnato**</dt></span><span class="sxs-lookup"><span data-stu-id="e139a-113"><dt>**WINBIO\_POOL\_UNASSIGNED**</dt></span></span> </dl> | <span data-ttu-id="e139a-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="e139a-114">Reserved.</span></span><br/>                                                                         |



## <a name="requirements"></a><span data-ttu-id="e139a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e139a-115">Requirements</span></span>



| <span data-ttu-id="e139a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e139a-116">Requirement</span></span> | <span data-ttu-id="e139a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e139a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e139a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e139a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e139a-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e139a-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e139a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e139a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e139a-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e139a-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e139a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e139a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e139a-123"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e139a-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e139a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e139a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e139a-125">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="e139a-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





