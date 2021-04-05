---
description: Connettersi a un'altra istanza di un motore remoto nel computer locale.
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IServerConnectionCallback:: ConnectToEngine'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125358"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span data-ttu-id="b023f-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>Metodo IServerConnectionCallback:: ConnectToEngine</span><span class="sxs-lookup"><span data-stu-id="b023f-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback::ConnectToEngine method</span></span>

<span data-ttu-id="b023f-104">Connettersi a un'altra istanza di un motore remoto nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="b023f-104">Connect to another instance of a remote engine on the local machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b023f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b023f-105">Syntax</span></span>


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a><span data-ttu-id="b023f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b023f-106">Parameters</span></span>

<span data-ttu-id="b023f-107">*bLegacyConnection* </span><span class="sxs-lookup"><span data-stu-id="b023f-107">*bLegacyConnection* </span></span>  
<span data-ttu-id="b023f-108">true se il motore utilizza è legacy, in caso contrario false.</span><span class="sxs-lookup"><span data-stu-id="b023f-108">true if the engine uses is legacy, otherwise false.</span></span>

<span data-ttu-id="b023f-109">*runAddress* </span><span class="sxs-lookup"><span data-stu-id="b023f-109">*runAddress* </span></span>  
<span data-ttu-id="b023f-110">Stringa COM contenente il nome del computer locale.</span><span class="sxs-lookup"><span data-stu-id="b023f-110">A COM string containing the name of the local machine.</span></span>

<span data-ttu-id="b023f-111">*ppEngineCreated* </span><span class="sxs-lookup"><span data-stu-id="b023f-111">*ppEngineCreated* </span></span>  
<span data-ttu-id="b023f-112">Al ritorno, l'indirizzo dell'istanza del motore.</span><span class="sxs-lookup"><span data-stu-id="b023f-112">On return, the address of the engine instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="b023f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b023f-113">Return value</span></span>

<span data-ttu-id="b023f-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b023f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b023f-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b023f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b023f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b023f-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b023f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b023f-117">Header</span></span></p></td><td><span data-ttu-id="b023f-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b023f-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b023f-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b023f-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b023f-120">**IServerConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="b023f-120">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
