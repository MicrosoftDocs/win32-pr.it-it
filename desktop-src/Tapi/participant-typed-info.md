---
description: "I membri dell'enum del \\_ partecipante \\_ informazioni tipizzate identificano il tipo di informazioni del partecipante recuperato dal metodo ITParticipant:: Get \\_ ParticipantTypedInfo. Questa enumerazione viene utilizzata dalle applicazioni che accedono al IPConf MSP."
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Enumerazione PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327489"
---
# <a name="participant_typed_info-enumeration"></a><span data-ttu-id="2c5d7-104">\_Enumerazione informazioni tipizzate partecipante \_</span><span class="sxs-lookup"><span data-stu-id="2c5d7-104">PARTICIPANT\_TYPED\_INFO enumeration</span></span>

<span data-ttu-id="2c5d7-105">\[**Partecipante \_ Le \_ informazioni tipizzate** non sono disponibili per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-105">\[**PARTICIPANT\_TYPED\_INFO** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c5d7-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2c5d7-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2c5d7-107">I membri dell'enum **del \_ partecipante \_ informazioni tipizzate** identificano il tipo di informazioni del partecipante recuperato dal metodo [**ITParticipant:: Get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2c5d7-107">The members of the **PARTICIPANT\_TYPED\_INFO** enum identify the type of participant information being retrieved by the [**ITParticipant::get\_ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) method.</span></span> <span data-ttu-id="2c5d7-108">Questa enumerazione viene utilizzata dalle applicazioni che accedono al [IPConf msp](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="2c5d7-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5d7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c5d7-109">Syntax</span></span>


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a><span data-ttu-id="2c5d7-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="2c5d7-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2c5d7-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**\_formato canonico PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI\_CANONICALNAME**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-112">Nome canonico del partecipante, ad esempio someone@example.com .</span><span class="sxs-lookup"><span data-stu-id="2c5d7-112">Canonical name of participant, such as someone@example.com.</span></span>

</dd> <dt>

<span data-ttu-id="2c5d7-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**\_nome PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI\_NAME**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-114">Nome visualizzabile del partecipante.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-114">Displayable name of participant.</span></span>

</dd> <dt>

<span data-ttu-id="2c5d7-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**\_EMAILADDRESS PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI\_EMAILADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-116">Indirizzo di posta elettronica del partecipante.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-116">Participant's email address.</span></span>

</dd> <dt>

<span data-ttu-id="2c5d7-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**\_PhoneNumber PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI\_PHONENUMBER**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-118">Indirizzo telefonico del partecipante.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-118">Participant's phone address.</span></span>

</dd> <dt>

<span data-ttu-id="2c5d7-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_località PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI\_LOCATION**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-120">Indirizzo geografico del partecipante.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-120">Participant's geographical address.</span></span>

</dd> <dt>

<span data-ttu-id="2c5d7-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_strumento PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI\_TOOL**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-122">Applicazione del partecipante.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-122">Participant's application.</span></span>

</dd> <dt>

<span data-ttu-id="2c5d7-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**\_Note PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI\_NOTES**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-124">Note relative al partecipante.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-124">Notes concerning participant.</span></span>

</dd> <dt>

<span data-ttu-id="2c5d7-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**\_privato PTI**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="2c5d7-126">Definisce un'estensione memoria SDES (Experimental Source Description) sperimentale o specifica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-126">Defines an experimental or application-specific Source Description (SDES) extension.</span></span> <span data-ttu-id="2c5d7-127">Per informazioni dettagliate, vedere RFC 1889.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-127">See RFC 1889 for details.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c5d7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c5d7-128">Requirements</span></span>



| <span data-ttu-id="2c5d7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c5d7-129">Requirement</span></span> | <span data-ttu-id="2c5d7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2c5d7-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5d7-131">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="2c5d7-131">TAPI version</span></span><br/> | <span data-ttu-id="2c5d7-132">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2c5d7-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2c5d7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c5d7-133">Header</span></span><br/>       | <dl> <span data-ttu-id="2c5d7-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c5d7-134"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c5d7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c5d7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5d7-136">**ITParticipant:: Get \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="2c5d7-136">**ITParticipant::get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[<span data-ttu-id="2c5d7-137">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="2c5d7-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="2c5d7-138">Interfacce MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="2c5d7-138">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




