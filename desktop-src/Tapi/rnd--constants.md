---
description: Le costanti seguenti possono essere restituite come errori.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Costanti RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327403"
---
# <a name="rnd_-constants"></a><span data-ttu-id="06d4a-103">\_Costanti Rnd</span><span class="sxs-lookup"><span data-stu-id="06d4a-103">RND\_ Constants</span></span>

<span data-ttu-id="06d4a-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06d4a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="06d4a-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="06d4a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="06d4a-106">Le costanti seguenti possono essere restituite come errori.</span><span class="sxs-lookup"><span data-stu-id="06d4a-106">The following constants may be returned as errors.</span></span>

<dl> <dt>

<span data-ttu-id="06d4a-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**\_ora non valida per RND \_**</span><span class="sxs-lookup"><span data-stu-id="06d4a-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="06d4a-108">0xe0000200</span><span class="sxs-lookup"><span data-stu-id="06d4a-108">0xe0000200</span></span>
</dt> <dt>



<span data-ttu-id="06d4a-109">Il valore di ora immesso non è valido.</span><span class="sxs-lookup"><span data-stu-id="06d4a-109">The time value entered is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06d4a-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**\_nome del \_ Server Rnd null \_**</span><span class="sxs-lookup"><span data-stu-id="06d4a-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND\_NULL\_SERVER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="06d4a-111">0xe0000201</span><span class="sxs-lookup"><span data-stu-id="06d4a-111">0xe0000201</span></span>
</dt> <dt>



<span data-ttu-id="06d4a-112">Il nome del server è **null**, probabilmente perché [**ITConferenceBlob:: init**](itconferenceblob-init.md) non è stato eseguito o non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="06d4a-112">The server name is **NULL**, probably because [**ITConferenceBlob::Init**](itconferenceblob-init.md) has not been run or did not succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06d4a-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ già \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="06d4a-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="06d4a-114">0xe0000202</span><span class="sxs-lookup"><span data-stu-id="06d4a-114">0xe0000202</span></span>
</dt> <dt>



<span data-ttu-id="06d4a-115">È stato chiamato il metodo [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) , ma esiste già una connessione.</span><span class="sxs-lookup"><span data-stu-id="06d4a-115">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method was called, but a connection already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="06d4a-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ non \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="06d4a-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="06d4a-117">0xe0000203</span><span class="sxs-lookup"><span data-stu-id="06d4a-117">0xe0000203</span></span>
</dt> <dt>



<span data-ttu-id="06d4a-118">Il metodo [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) non è stato chiamato o non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="06d4a-118">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method has not been called, or failed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06d4a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06d4a-119">Requirements</span></span>



| <span data-ttu-id="06d4a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="06d4a-120">Requirement</span></span> | <span data-ttu-id="06d4a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="06d4a-121">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06d4a-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="06d4a-122">TAPI version</span></span><br/> | <span data-ttu-id="06d4a-123">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="06d4a-123">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="06d4a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06d4a-124">Header</span></span><br/>       | <dl> <span data-ttu-id="06d4a-125"><dt>Rnderr. h</dt></span><span class="sxs-lookup"><span data-stu-id="06d4a-125"><dt>Rnderr.h</dt></span></span> </dl> |



 

 




