---
description: Visualizza un messaggio di errore nel fumetto suggerimento associato al controllo dell'indirizzo di rete.
title: Messaggio NCM_DISPLAYERRORTIP (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993776"
---
# <a name="ncm_displayerrortip-message"></a><span data-ttu-id="c9f08-103">\_Messaggio NCM DISPLAYERRORTIP</span><span class="sxs-lookup"><span data-stu-id="c9f08-103">NCM\_DISPLAYERRORTIP message</span></span>

<span data-ttu-id="c9f08-104">Visualizza un messaggio di errore nel fumetto suggerimento associato al controllo dell'indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="c9f08-104">Displays an error message in the balloon tip associated with the network address control.</span></span>


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="c9f08-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9f08-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f08-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9f08-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c9f08-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c9f08-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c9f08-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9f08-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c9f08-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c9f08-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9f08-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9f08-110">Return value</span></span>

<span data-ttu-id="c9f08-111">Se il messaggio ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c9f08-111">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9f08-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9f08-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9f08-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9f08-113">Remarks</span></span>

<span data-ttu-id="c9f08-114">Inviare questo messaggio per visualizzare un messaggio di errore quando un indirizzo digitato nel controllo non viene convalidato in base ai tipi di indirizzi di rete consentiti impostati con il messaggio [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f08-114">Send this message to display an error message when an address typed into the control does not validate against the allowed network address types set with the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message.</span></span> <span data-ttu-id="c9f08-115">Usare il messaggio [**NCM \_ GetAddress**](ncm-getaddress.md) per convalidare l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c9f08-115">Use the [**NCM\_GETADDRESS**](ncm-getaddress.md) message to validate the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f08-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9f08-116">Requirements</span></span>



| <span data-ttu-id="c9f08-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9f08-117">Requirement</span></span> | <span data-ttu-id="c9f08-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c9f08-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f08-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9f08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f08-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9f08-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9f08-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9f08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f08-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9f08-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9f08-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9f08-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9f08-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9f08-124"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9f08-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9f08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f08-126">**\_DisplayErrorTip NetAddr**</span><span class="sxs-lookup"><span data-stu-id="c9f08-126">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




