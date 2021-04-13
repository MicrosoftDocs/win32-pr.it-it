---
title: Costanti WINBIO_BIR_FIELD (tipi WinBio \_ . h)
description: Specificare una maschera di maschera.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340732"
---
# <a name="winbio_bir_field-constants"></a><span data-ttu-id="8350c-103">\_Costanti di \_ campo WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="8350c-103">WINBIO\_BIR\_FIELD Constants</span></span>

<span data-ttu-id="8350c-104">Le costanti seguenti vengono usate per creare una maschera di maschera per il membro **ValidFields** della struttura dell' [**\_ \_ intestazione WINBIO bir**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="8350c-104">The following constants are used to create a bitmask for the **ValidFields** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="8350c-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="8350c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="8350c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8350c-106">Description</span></span>                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <span data-ttu-id="8350c-107"><dt>**WINBIO \_ \_Numero di \_ sottointestazioni \_ del campo bir**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-107"><dt>**WINBIO\_BIR\_FIELD\_SUBHEAD\_COUNT**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="8350c-108">Fornito per conformità con NISTIR 6529-A, il formato comune CBEFF (Biometric Exchange formats Framework) A, ma non usato.</span><span class="sxs-lookup"><span data-stu-id="8350c-108">Provided for conformity with NISTIR 6529-A, the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A, but not used.</span></span><br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <span data-ttu-id="8350c-109"><dt>**WINBIO \_ \_ \_ \_ ID prodotto campo bir**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-109"><dt>**WINBIO\_BIR\_FIELD\_PRODUCT\_ID**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="8350c-110">Il membro **ProductID** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-110">The **ProductId** member is valid.</span></span><br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <span data-ttu-id="8350c-111"><dt>**WINBIO \_ \_ \_ \_ ID patron del campo bir**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-111"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_ID**</dt> <dt>0x0004</dt></span></span> </dl>                                      | <span data-ttu-id="8350c-112">Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.</span><span class="sxs-lookup"><span data-stu-id="8350c-112">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <span data-ttu-id="8350c-113"><dt>**WINBIO \_ \_ \_ Indice del campo bir**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-113"><dt>**WINBIO\_BIR\_FIELD\_INDEX**</dt> <dt>0x0008</dt></span></span> </dl>                                                   | <span data-ttu-id="8350c-114">Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.</span><span class="sxs-lookup"><span data-stu-id="8350c-114">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <span data-ttu-id="8350c-115"><dt>**WINBIO \_ \_ \_ \_ Data creazione campo bir**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-115"><dt>**WINBIO\_BIR\_FIELD\_CREATION\_DATE**</dt> <dt>0x0010</dt></span></span> </dl>                          | <span data-ttu-id="8350c-116">Il membro **CreationDate** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-116">The **CreationDate** member is valid.</span></span><br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <span data-ttu-id="8350c-117"><dt>**WINBIO \_ \_Periodo di \_ validità \_ del campo bir**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-117"><dt>**WINBIO\_BIR\_FIELD\_VALIDITY\_PERIOD**</dt> <dt>0x0020</dt></span></span> </dl>                    | <span data-ttu-id="8350c-118">Il membro **ValidityPeriod** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-118">The **ValidityPeriod** member is valid.</span></span><br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <span data-ttu-id="8350c-119"><dt>**WINBIO \_ \_ \_ \_ Tipo biometrico del campo bir**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-119"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_TYPE**</dt> <dt>0x0040</dt></span></span> </dl>                       | <span data-ttu-id="8350c-120">Il membro del **tipo** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-120">The **Type** member is valid.</span></span><br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <span data-ttu-id="8350c-121"><dt>**WINBIO \_ \_SOTTOtipo \_ biometrico \_ del campo bir**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-121"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_SUBTYPE**</dt> <dt>0x0080</dt></span></span> </dl>              | <span data-ttu-id="8350c-122">Il membro del **sottotipo** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-122">The **Subtype** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <span data-ttu-id="8350c-123"><dt>**WINBIO \_ BIR \_ Field \_ CBEFF \_ header \_ versione**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-123"><dt>**WINBIO\_BIR\_FIELD\_CBEFF\_HEADER\_VERSION**</dt> <dt>0x0100</dt></span></span> </dl>    | <span data-ttu-id="8350c-124">Il membro **HeaderVersion** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-124">The **HeaderVersion** member is valid.</span></span><br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <span data-ttu-id="8350c-125"><dt>**WINBIO \_ \_Versione di \_ \_ intestazione patron \_ del campo bir**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-125"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_HEADER\_VERSION**</dt> <dt>0x0200</dt></span></span> </dl> | <span data-ttu-id="8350c-126">Il membro **PatronHeaderVersion** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-126">The **PatronHeaderVersion** member is valid.</span></span><br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <span data-ttu-id="8350c-127"><dt>**WINBIO \_ Il \_ campo bir 0x0400 \_ \_ scopo biometrico**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8350c-127"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_PURPOSE**</dt> <dt>0x0400</dt></span></span> </dl>              | <span data-ttu-id="8350c-128">Il membro **scopo** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-128">The **Purpose** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <span data-ttu-id="8350c-129"><dt>**WINBIO \_ \_ \_ \_ Condizione biometrica del campo bir**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-129"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_CONDITION**</dt> <dt>0x0800</dt></span></span> </dl>        | <span data-ttu-id="8350c-130">Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.</span><span class="sxs-lookup"><span data-stu-id="8350c-130">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <span data-ttu-id="8350c-131"><dt>**WINBIO \_ \_ \_ Qualità del campo bir**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-131"><dt>**WINBIO\_BIR\_FIELD\_QUALITY**</dt> <dt>0x1000</dt></span></span> </dl>                                             | <span data-ttu-id="8350c-132">Il membro **dataquality** è valido.</span><span class="sxs-lookup"><span data-stu-id="8350c-132">The **DataQuality** member is valid.</span></span><br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <span data-ttu-id="8350c-133"><dt>**WINBIO \_ \_ \_ Creatore del campo bir**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-133"><dt>**WINBIO\_BIR\_FIELD\_CREATOR**</dt> <dt>0x2000</dt></span></span> </dl>                                             | <span data-ttu-id="8350c-134">Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.</span><span class="sxs-lookup"><span data-stu-id="8350c-134">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <span data-ttu-id="8350c-135"><dt>**WINBIO \_ 0x4000 \_ di \_ test del campo bir**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8350c-135"><dt>**WINBIO\_BIR\_FIELD\_CHALLENGE**</dt> <dt>0x4000</dt></span></span> </dl>                                       | <span data-ttu-id="8350c-136">Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.</span><span class="sxs-lookup"><span data-stu-id="8350c-136">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <span data-ttu-id="8350c-137"><dt>**WINBIO \_ \_ \_ Payload campo bir**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-137"><dt>**WINBIO\_BIR\_FIELD\_PAYLOAD**</dt> <dt>0x8000</dt></span></span> </dl>                                             | <span data-ttu-id="8350c-138">Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.</span><span class="sxs-lookup"><span data-stu-id="8350c-138">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="8350c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8350c-139">Requirements</span></span>



| <span data-ttu-id="8350c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8350c-140">Requirement</span></span> | <span data-ttu-id="8350c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8350c-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8350c-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8350c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8350c-143">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8350c-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="8350c-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8350c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8350c-145">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8350c-145">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8350c-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8350c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8350c-147"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8350c-147"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8350c-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8350c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8350c-149">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="8350c-149">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





