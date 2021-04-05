---
title: Costanti WINBIO_CAPABILITY (tipi WinBio \_ . h)
description: Sottotipi del sensore di impronta digitale.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873849"
---
# <a name="winbio_capability-constants"></a><span data-ttu-id="266da-103">\_Costanti della funzionalità WINBIO</span><span class="sxs-lookup"><span data-stu-id="266da-103">WINBIO\_CAPABILITY Constants</span></span>

<span data-ttu-id="266da-104">I sottotipi di sensore impronta digitale seguenti sono valori di **\_ capacità WINBIO** che possono essere usati come maschera di maschera per il parametro *capabilities* della struttura [**\_ \_ dello schema dell'unità WINBIO**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="266da-104">The following fingerprint sensor sub types are **WINBIO\_CAPABILITIES** values that can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="266da-105">Che fanno riferimento alle funzionalità del sensore di onboarding.</span><span class="sxs-lookup"><span data-stu-id="266da-105">These refer to the onboard sensor capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="266da-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="266da-106">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="266da-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="266da-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <span data-ttu-id="266da-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-108"><dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-109">Il sensore può acquisire i dati biometrici.</span><span class="sxs-lookup"><span data-stu-id="266da-109">The sensor can capture biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <span data-ttu-id="266da-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-110"><dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-111">Il sensore può corrispondere ai dati biometrici a un'identità.</span><span class="sxs-lookup"><span data-stu-id="266da-111">The sensor can match biometric data to an identity.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <span data-ttu-id="266da-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-112"><dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-113">Il sensore contiene un database di onboarding.</span><span class="sxs-lookup"><span data-stu-id="266da-113">The sensor contains an onboard database.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <span data-ttu-id="266da-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-114"><dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-115">Il sensore può eseguire l'elaborazione biometrica.</span><span class="sxs-lookup"><span data-stu-id="266da-115">The sensor can perform biometric processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <span data-ttu-id="266da-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-116"><dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-117">Il sensore può crittografare i dati biometrici.</span><span class="sxs-lookup"><span data-stu-id="266da-117">The sensor can encrypt biometric data.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <span data-ttu-id="266da-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-118"><dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-119">Il sensore può fungere da pad del mouse.</span><span class="sxs-lookup"><span data-stu-id="266da-119">The sensor can act as a mouse pad.</span></span> <span data-ttu-id="266da-120">Non supportato attualmente.</span><span class="sxs-lookup"><span data-stu-id="266da-120">This is currently not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <span data-ttu-id="266da-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-121"><dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-122">Il sensore contiene una luce indicatore.</span><span class="sxs-lookup"><span data-stu-id="266da-122">The sensor contains an indicator light.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <span data-ttu-id="266da-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="266da-123"><dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="266da-124">L'adattatore del sensore gestisce la propria connessione all'hardware biometrico.</span><span class="sxs-lookup"><span data-stu-id="266da-124">The sensor adapter manages its own connection to the biometric hardware.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="266da-125">Questa costante si applica solo a Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="266da-125">This constant applies only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="266da-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="266da-126">Requirements</span></span>



| <span data-ttu-id="266da-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="266da-127">Requirement</span></span> | <span data-ttu-id="266da-128">Valore</span><span class="sxs-lookup"><span data-stu-id="266da-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="266da-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="266da-129">Minimum supported client</span></span><br/> | <span data-ttu-id="266da-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="266da-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="266da-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="266da-131">Minimum supported server</span></span><br/> | <span data-ttu-id="266da-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="266da-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                  |
| <span data-ttu-id="266da-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="266da-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="266da-134"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="266da-134"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="266da-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="266da-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="266da-136">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="266da-136">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="266da-137">**\_schema unità \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="266da-137">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





