---
description: Il tipo di indirizzo identifica il formato dell'indirizzo, ad esempio il numero di telefono standard o l'indirizzo di posta elettronica. Solo le applicazioni che negoziano la versione 3,0 o successiva di TAPI possono usare i tipi di indirizzo.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Costanti LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327786"
---
# <a name="lineaddresstype_-constants"></a><span data-ttu-id="485c7-104">\_Costanti LINEADDRESSTYPE</span><span class="sxs-lookup"><span data-stu-id="485c7-104">LINEADDRESSTYPE\_ Constants</span></span>

<span data-ttu-id="485c7-105">Il tipo di indirizzo identifica il formato dell'indirizzo, ad esempio il numero di telefono standard o l'indirizzo di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="485c7-105">The address type identifies address format, such as standard phone number or e-mail address.</span></span> <span data-ttu-id="485c7-106">Solo le applicazioni che negoziano la versione 3,0 o successiva di TAPI possono usare i tipi di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="485c7-106">Only applications that negotiate TAPI version 3.0 or higher can use address types.</span></span>

<dl> <dt>

<span data-ttu-id="485c7-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**\_PhoneNumber LINEADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="485c7-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE\_PHONENUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="485c7-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="485c7-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="485c7-109">Tipo di indirizzo è un numero di telefono standard.</span><span class="sxs-lookup"><span data-stu-id="485c7-109">Address type is a standard phone number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="485c7-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**\_SDP LINEADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="485c7-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE\_SDP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="485c7-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="485c7-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="485c7-112">Tipo di indirizzo è la conferenza SDP (Session Description Protocol).</span><span class="sxs-lookup"><span data-stu-id="485c7-112">Address type is Session Description Protocol (SDP) conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="485c7-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EmailName**</span><span class="sxs-lookup"><span data-stu-id="485c7-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE\_EMAILNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="485c7-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="485c7-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="485c7-115">Tipo di indirizzo è un nome di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="485c7-115">Address type is an e-mail name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="485c7-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ DomainName**</span><span class="sxs-lookup"><span data-stu-id="485c7-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="485c7-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="485c7-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="485c7-118">Tipo di indirizzo è un nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="485c7-118">Address type is a domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="485c7-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="485c7-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE\_IPADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="485c7-120">0x00000010</span><span class="sxs-lookup"><span data-stu-id="485c7-120">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="485c7-121">Il tipo di indirizzo è un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="485c7-121">Address type is an IP address.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="485c7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="485c7-122">Requirements</span></span>



| <span data-ttu-id="485c7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="485c7-123">Requirement</span></span> | <span data-ttu-id="485c7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="485c7-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="485c7-125">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="485c7-125">TAPI version</span></span><br/> | <span data-ttu-id="485c7-126">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="485c7-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="485c7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="485c7-127">Header</span></span><br/>       | <dl> <span data-ttu-id="485c7-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="485c7-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




