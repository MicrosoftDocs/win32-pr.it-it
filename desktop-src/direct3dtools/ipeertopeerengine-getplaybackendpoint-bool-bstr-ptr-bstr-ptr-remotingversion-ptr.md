---
description: Ottiene l'indirizzo dell'endpoint di un motore remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPeerToPeerEngine:: GetPlaybackEndpoint'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6ee25dbd456086227e88fcb8bf7708a39e26eb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521145"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span data-ttu-id="618df-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>Metodo IPeerToPeerEngine:: GetPlaybackEndpoint</span><span class="sxs-lookup"><span data-stu-id="618df-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint method</span></span>

<span data-ttu-id="618df-104">Ottiene l'indirizzo dell'endpoint di un motore remoto.</span><span class="sxs-lookup"><span data-stu-id="618df-104">Gets the endpoint address of a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="618df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="618df-105">Syntax</span></span>


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="618df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="618df-106">Parameters</span></span>

<span data-ttu-id="618df-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="618df-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="618df-108">true se il motore remoto utilizza l'autenticazione di. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="618df-108">true if the remote engine uses authentication; otherwise, false.</span></span>

<span data-ttu-id="618df-109">*pEndpoint* </span><span class="sxs-lookup"><span data-stu-id="618df-109">*pEndpoint* </span></span>  
<span data-ttu-id="618df-110">Al ritorno, una stringa COM contenente l'indirizzo dell'endpoint del computer di riproduzione remoto.</span><span class="sxs-lookup"><span data-stu-id="618df-110">On return, a COM string containing the endpoint address of the remote playback machine.</span></span>

<span data-ttu-id="618df-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="618df-111">*sessionKey* </span></span>  
<span data-ttu-id="618df-112">Al ritorno, una stringa COM contenente la chiave di sessione utilizzata per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="618df-112">On return, a COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="618df-113">*pRemoteVersion* </span><span class="sxs-lookup"><span data-stu-id="618df-113">*pRemoteVersion* </span></span>  
<span data-ttu-id="618df-114">Al ritorno, la versione del motore remoto.</span><span class="sxs-lookup"><span data-stu-id="618df-114">On return, the version of the remote engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="618df-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="618df-115">Return value</span></span>

<span data-ttu-id="618df-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="618df-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="618df-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="618df-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="618df-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="618df-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="618df-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="618df-119">Header</span></span></p></td><td><span data-ttu-id="618df-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="618df-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="618df-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="618df-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="618df-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="618df-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
