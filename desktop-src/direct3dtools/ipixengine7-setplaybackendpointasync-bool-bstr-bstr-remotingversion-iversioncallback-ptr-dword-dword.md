---
description: Imposta in modo asincrono l'indirizzo dell'endpoint utilizzato per la connessione a un motore remoto.
MS-HAID: vspixengine.IPixEngine7\_SetPlaybackEndpointAsync\_BOOL\_BSTR\_BSTR\_RemotingVersion\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixEngine7:: SetPlaybackEndpointAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4F76EFFF-F3CB-4BEA-999F-639876C7F792
api_name:
- IPixEngine7.SetPlaybackEndpointAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2e0970b1a2a786c828a24efef0ae9e4057dbe2cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747386"
---
# <a name="span-idvspixengineipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dwordspanipixengine7setplaybackendpointasync-method"></a><span data-ttu-id="934f8-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>Metodo IPixEngine7:: SetPlaybackEndpointAsync</span><span class="sxs-lookup"><span data-stu-id="934f8-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7::SetPlaybackEndpointAsync method</span></span>

<span data-ttu-id="934f8-104">Imposta in modo asincrono l'indirizzo dell'endpoint utilizzato per la connessione a un motore remoto.</span><span class="sxs-lookup"><span data-stu-id="934f8-104">Asynchronously sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="934f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="934f8-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpointAsync(
   BOOL              bUseAuthentication,
   BSTR              endpoint,
   BSTR              sessionKey,
   RemotingVersion   remoteVersion,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="934f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="934f8-106">Parameters</span></span>

<span data-ttu-id="934f8-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="934f8-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="934f8-108">true per utilizzare l'autenticazione; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="934f8-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="934f8-109">*endpoint* </span><span class="sxs-lookup"><span data-stu-id="934f8-109">*endpoint* </span></span>  
<span data-ttu-id="934f8-110">Stringa COM che contiene l'indirizzo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="934f8-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="934f8-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="934f8-111">*sessionKey* </span></span>  
<span data-ttu-id="934f8-112">Stringa COM contenente la chiave di sessione utilizzata per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="934f8-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="934f8-113">*remoteVersion* </span><span class="sxs-lookup"><span data-stu-id="934f8-113">*remoteVersion* </span></span>  
<span data-ttu-id="934f8-114">Specifica la versione del motore remoto da usare.</span><span class="sxs-lookup"><span data-stu-id="934f8-114">Specifies the version of the remote engine to use.</span></span>

<span data-ttu-id="934f8-115">*versionCallback* </span><span class="sxs-lookup"><span data-stu-id="934f8-115">*versionCallback* </span></span>  
<span data-ttu-id="934f8-116">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="934f8-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="934f8-117">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="934f8-117">*requestCookie* </span></span>  
<span data-ttu-id="934f8-118">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="934f8-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="934f8-119">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="934f8-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="934f8-120">Non usato.</span><span class="sxs-lookup"><span data-stu-id="934f8-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="934f8-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="934f8-121">Return value</span></span>

<span data-ttu-id="934f8-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="934f8-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="934f8-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="934f8-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="934f8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="934f8-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="934f8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="934f8-125">Header</span></span></p></td><td><span data-ttu-id="934f8-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="934f8-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="934f8-127"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="934f8-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="934f8-128">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="934f8-128">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
