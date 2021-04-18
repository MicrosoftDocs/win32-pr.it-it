---
description: Callback che invia una notifica all'host dei messaggi restituiti dalla richiesta associata.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixErrorCallback:: MessagesCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303950"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span data-ttu-id="01b54-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>Metodo IPixErrorCallback:: MessagesCallback</span><span class="sxs-lookup"><span data-stu-id="01b54-103"><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>IPixErrorCallback::MessagesCallback method</span></span>

<span data-ttu-id="01b54-104">Callback che invia una notifica all'host dei messaggi restituiti dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="01b54-104">A callback that notifies the host of messages returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b54-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01b54-105">Syntax</span></span>


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a><span data-ttu-id="01b54-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01b54-106">Parameters</span></span>

<span data-ttu-id="01b54-107">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="01b54-107">*count* </span></span>  
<span data-ttu-id="01b54-108">Numero di messaggi.</span><span class="sxs-lookup"><span data-stu-id="01b54-108">The number of messages.</span></span>

<span data-ttu-id="01b54-109">*\_messaggi count0* </span><span class="sxs-lookup"><span data-stu-id="01b54-109">*count0\_messages* </span></span>  
<span data-ttu-id="01b54-110">Messaggi.</span><span class="sxs-lookup"><span data-stu-id="01b54-110">The messages.</span></span>

## <a name="return-value"></a><span data-ttu-id="01b54-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01b54-111">Return value</span></span>

<span data-ttu-id="01b54-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01b54-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01b54-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01b54-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b54-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01b54-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="01b54-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01b54-115">Header</span></span></p></td><td><span data-ttu-id="01b54-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="01b54-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="01b54-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="01b54-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="01b54-118">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="01b54-118">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
