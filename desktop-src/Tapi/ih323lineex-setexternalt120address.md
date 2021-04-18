---
description: Il metodo SetExternalT120Address viene chiamato da un'applicazione per configurare un indirizzo T. 120 esterno per lo scambio di dati.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'Metodo IH323LineEx:: SetExternalT120Address (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326146"
---
# <a name="ih323lineexsetexternalt120address-method"></a><span data-ttu-id="111d5-103">Metodo IH323LineEx:: SetExternalT120Address</span><span class="sxs-lookup"><span data-stu-id="111d5-103">IH323LineEx::SetExternalT120Address method</span></span>

<span data-ttu-id="111d5-104">\[**SetExternalT120Address** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="111d5-104">\[**SetExternalT120Address** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="111d5-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="111d5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="111d5-106">Il metodo **SetExternalT120Address** viene chiamato da un'applicazione per configurare un indirizzo T. 120 esterno per lo scambio di dati.</span><span class="sxs-lookup"><span data-stu-id="111d5-106">The **SetExternalT120Address** method is called by an application to configure an external T.120 address for data exchange.</span></span> <span data-ttu-id="111d5-107">La funzionalità T. 120 verrà annunciata durante la negoziazione H. 245 e l'indirizzo verrà usato nel riconoscimento del canale della logica aperto, in modo che l'altro endpoint possa configurare sessioni T. 120 con il servizio in ascolto su tale indirizzo.</span><span class="sxs-lookup"><span data-stu-id="111d5-107">T.120 capability will be advertised during the H.245 negotiation, and the address will be used in the open logic channel acknowledgement so that the other endpoint can set up T.120 sessions with the service listening on that address.</span></span> <span data-ttu-id="111d5-108">Se questa funzione non viene chiamata, il provider di servizi H. 323 non annuncia la funzionalità T. 120.</span><span class="sxs-lookup"><span data-stu-id="111d5-108">If this function is not called, the H.323 service provider will not advertise T.120 capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="111d5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="111d5-109">Syntax</span></span>


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a><span data-ttu-id="111d5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="111d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="111d5-111">*fEnable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="111d5-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="111d5-112">**True** per abilitare la funzionalità T. 120; **False** per disabilitare la funzionalità T. 120.</span><span class="sxs-lookup"><span data-stu-id="111d5-112">**TRUE** to enable T.120 capability; **FALSE** to disable T.120 capability.</span></span>

</dd> <dt>

<span data-ttu-id="111d5-113">*dwIP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="111d5-113">*dwIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="111d5-114">**DWORD** che contiene l'indirizzo IP nell'ordine dei byte dell'host del servizio esterno T. 120.</span><span class="sxs-lookup"><span data-stu-id="111d5-114">**DWORD** containing the IP address in host byte order of the external T.120 service.</span></span>

</dd> <dt>

<span data-ttu-id="111d5-115">*wPort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="111d5-115">*wPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="111d5-116">**Parola** contenente la porta del servizio esterno T. 120.</span><span class="sxs-lookup"><span data-stu-id="111d5-116">**WORD** containing the port of the external T.120 service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="111d5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="111d5-117">Return value</span></span>

<span data-ttu-id="111d5-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="111d5-118">This method can return one of these values.</span></span>



| <span data-ttu-id="111d5-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="111d5-119">Return code</span></span>                                                                          | <span data-ttu-id="111d5-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="111d5-120">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="111d5-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="111d5-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="111d5-122">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="111d5-122">Method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="111d5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="111d5-123">Requirements</span></span>



| <span data-ttu-id="111d5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="111d5-124">Requirement</span></span> | <span data-ttu-id="111d5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="111d5-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="111d5-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="111d5-126">TAPI version</span></span><br/> | <span data-ttu-id="111d5-127">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="111d5-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="111d5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="111d5-128">Header</span></span><br/>       | <dl> <span data-ttu-id="111d5-129"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="111d5-129"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="111d5-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="111d5-130">Library</span></span><br/>      | <dl> <span data-ttu-id="111d5-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="111d5-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="111d5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="111d5-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="111d5-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="111d5-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




