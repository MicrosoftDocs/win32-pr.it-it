---
description: Imposta l'indirizzo dell'endpoint utilizzato per la connessione a un motore remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPeerToPeerEngine:: SetPlaybackEndpoint'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbec4826fb2659604a4b9f4388beed1829b42770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482405"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span data-ttu-id="448ad-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>Metodo IPeerToPeerEngine:: SetPlaybackEndpoint</span><span class="sxs-lookup"><span data-stu-id="448ad-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine::SetPlaybackEndpoint method</span></span>

<span data-ttu-id="448ad-104">Imposta l'indirizzo dell'endpoint utilizzato per la connessione a un motore remoto.</span><span class="sxs-lookup"><span data-stu-id="448ad-104">Sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="448ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="448ad-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="448ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="448ad-106">Parameters</span></span>

<span data-ttu-id="448ad-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="448ad-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="448ad-108">true per utilizzare l'autenticazione; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="448ad-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="448ad-109">*endpoint* </span><span class="sxs-lookup"><span data-stu-id="448ad-109">*endpoint* </span></span>  
<span data-ttu-id="448ad-110">Stringa COM che contiene l'indirizzo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="448ad-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="448ad-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="448ad-111">*sessionKey* </span></span>  
<span data-ttu-id="448ad-112">Stringa COM contenente la chiave di sessione utilizzata per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="448ad-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="448ad-113">*remoteVersion* </span><span class="sxs-lookup"><span data-stu-id="448ad-113">*remoteVersion* </span></span>  
<span data-ttu-id="448ad-114">Specifica la versione del motore remoto da usare.</span><span class="sxs-lookup"><span data-stu-id="448ad-114">Specifies the version of the remote engine to use.</span></span>

## <a name="return-value"></a><span data-ttu-id="448ad-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="448ad-115">Return value</span></span>

<span data-ttu-id="448ad-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="448ad-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="448ad-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="448ad-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="448ad-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="448ad-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="448ad-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="448ad-119">Header</span></span></p></td><td><span data-ttu-id="448ad-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="448ad-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="448ad-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="448ad-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="448ad-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="448ad-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
