---
title: Messaggio CQPM_CLEARFORM (cmnquery. h)
description: Inviato alla funzione di callback CQPageProc di una query per la pagina di estensione quando il contenuto della pagina deve essere reimpostato sui valori predefiniti.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- Messaggio CQPM_CLEARFORM Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963839"
---
# <a name="cqpm_clearform-message"></a><span data-ttu-id="9e715-104">\_Messaggio CQPM CLEARFORM</span><span class="sxs-lookup"><span data-stu-id="9e715-104">CQPM\_CLEARFORM message</span></span>

<span data-ttu-id="9e715-105">Il messaggio **CQPM \_ CLEARFORM** viene inviato alla funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) di una query per la pagina di estensione quando il contenuto della pagina deve essere reimpostato sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="9e715-105">The **CQPM\_CLEARFORM** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query for extension page when the contents of the page should be reset to the default values.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e715-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e715-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e715-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e715-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9e715-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e715-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e715-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e715-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9e715-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e715-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e715-111">Return value</span></span>

<span data-ttu-id="9e715-112">Restituisce **\_ OK** se l'esito è positivo o un codice di errore **HRESULT** standard.</span><span class="sxs-lookup"><span data-stu-id="9e715-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e715-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e715-113">Requirements</span></span>



| <span data-ttu-id="9e715-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e715-114">Requirement</span></span> | <span data-ttu-id="9e715-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9e715-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e715-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e715-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e715-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e715-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="9e715-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e715-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e715-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e715-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="9e715-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e715-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e715-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e715-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e715-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e715-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e715-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="9e715-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





