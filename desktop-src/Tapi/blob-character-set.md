---
description: L' \_ enumerazione del set di caratteri BLOB \_ indica il set di caratteri usato dal BLOB di conferenza corrente.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Enumerazione BLOB_CHARACTER_SET (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329092"
---
# <a name="blob_character_set-enumeration"></a><span data-ttu-id="ee900-103">\_Enumerazione set di caratteri BLOB \_</span><span class="sxs-lookup"><span data-stu-id="ee900-103">BLOB\_CHARACTER\_SET enumeration</span></span>

<span data-ttu-id="ee900-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ee900-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ee900-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ee900-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ee900-106">L'enumerazione del **\_ \_ set di caratteri BLOB** indica il set di caratteri usato dal BLOB di conferenza corrente.</span><span class="sxs-lookup"><span data-stu-id="ee900-106">The **BLOB\_CHARACTER\_SET** enum indicates the character set used by the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee900-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee900-107">Syntax</span></span>


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a><span data-ttu-id="ee900-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="ee900-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee900-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**\_ASCII BCS**</span><span class="sxs-lookup"><span data-stu-id="ee900-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS\_ASCII**</span></span>
</dt> <dd>

<span data-ttu-id="ee900-110">Formato ASCII standard.</span><span class="sxs-lookup"><span data-stu-id="ee900-110">Standard ASCII format.</span></span>

</dd> <dt>

<span data-ttu-id="ee900-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**\_UTF7 BCS**</span><span class="sxs-lookup"><span data-stu-id="ee900-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS\_UTF7**</span></span>
</dt> <dd>

<span data-ttu-id="ee900-112">Formato di trasformazione a sette bit di Unicode.</span><span class="sxs-lookup"><span data-stu-id="ee900-112">Seven-bit transformation format of Unicode.</span></span> <span data-ttu-id="ee900-113">Per informazioni dettagliate su questo formato, effettuare una ricerca Internet per RFC 1642.</span><span class="sxs-lookup"><span data-stu-id="ee900-113">For details on this format, conduct an Internet search for RFC 1642.</span></span>

</dd> <dt>

<span data-ttu-id="ee900-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**\_UTF8 BCS**</span><span class="sxs-lookup"><span data-stu-id="ee900-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS\_UTF8**</span></span>
</dt> <dd>

<span data-ttu-id="ee900-115">Formato di trasformazione UCS 8.</span><span class="sxs-lookup"><span data-stu-id="ee900-115">UCS Transformation Format 8.</span></span> <span data-ttu-id="ee900-116">Per informazioni dettagliate su questo formato, eseguire una ricerca Internet per il documento ISO (il organizzazione internazionale per la standardizzazione) e IEC (il International Electrotechnical Commission) ISO/IEC JTC1/SC2/WG2 N 1036, data 1 agosto 1994, dall'editor di progetto WG2.</span><span class="sxs-lookup"><span data-stu-id="ee900-116">For details on this format, conduct an Internet search for ISO (the International Organization for Standardization) and IEC (the International Electrotechnical Commission) document ISO/IEC JTC1/SC2/WG2 N 1036, dated August 1, 1994, by WG2 Project Editor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee900-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee900-117">Requirements</span></span>



| <span data-ttu-id="ee900-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee900-118">Requirement</span></span> | <span data-ttu-id="ee900-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ee900-119">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee900-120">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ee900-120">TAPI version</span></span><br/> | <span data-ttu-id="ee900-121">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ee900-121">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="ee900-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee900-122">Header</span></span><br/>       | <dl> <span data-ttu-id="ee900-123"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee900-123"><dt>Sdpblb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee900-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee900-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee900-125">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="ee900-125">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[<span data-ttu-id="ee900-126">**Ottieni \_ caratteri**</span><span class="sxs-lookup"><span data-stu-id="ee900-126">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)
</dt> <dt>

[<span data-ttu-id="ee900-127">**Init**</span><span class="sxs-lookup"><span data-stu-id="ee900-127">**Init**</span></span>](itconferenceblob-init.md)
</dt> <dt>

[<span data-ttu-id="ee900-128">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="ee900-128">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




