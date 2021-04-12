---
title: Costanti WINBIO_BIR_DATA_FLAGS (tipi WinBio \_ . h)
description: Consente di specificare la condizione dei dati.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400926"
---
# <a name="winbio_bir_data_flags-constants"></a><span data-ttu-id="6d423-103">\_ \_ Costanti flag di dati WINBIO bir \_</span><span class="sxs-lookup"><span data-stu-id="6d423-103">WINBIO\_BIR\_DATA\_FLAGS Constants</span></span>

<span data-ttu-id="6d423-104">Le costanti seguenti vengono usate dal membro **Dataflags** della struttura dell' [**intestazione WINBIO \_ Bir \_**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="6d423-104">The following constants are used by the **DataFlags** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="6d423-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="6d423-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="6d423-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d423-106">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="6d423-107"><dt>**WINBIO \_ 0x02 \_ \_ privacy del flag di dati**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d423-107"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>0x02</dt></span></span> </dl>                                       | <span data-ttu-id="6d423-108">I dati sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="6d423-108">The data is encrypted.</span></span><br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="6d423-109"><dt>**WINBIO \_ \_ \_ Integrità del flag di dati**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6d423-109"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>0x01</dt></span></span> </dl>                                 | <span data-ttu-id="6d423-110">I dati sono firmati digitalmente o sono protetti da un codice MAC (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="6d423-110">The data is digitally signed or is protected by a message authentication code (MAC).</span></span><br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="6d423-111"><dt>**WINBIO \_ FLAG di dati con \_ \_ segno**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="6d423-111"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>0x04</dt></span></span> </dl>                                          | <span data-ttu-id="6d423-112">Se vengono impostati questo flag e il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , i dati vengono firmati.</span><span class="sxs-lookup"><span data-stu-id="6d423-112">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="6d423-113">Se questo flag non è impostato ma è impostato il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , viene calcolato un Mac sui dati.</span><span class="sxs-lookup"><span data-stu-id="6d423-113">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed on the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="6d423-114"><dt>**WINBIO \_ FLAG di dati 0x20 \_ \_ RAW**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d423-114"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>0x20</dt></span></span> </dl>                                                   | <span data-ttu-id="6d423-115">I dati sono nel formato con cui sono stati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="6d423-115">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="6d423-116"><dt>**WINBIO \_ 0x40 \_ \_ intermedio del flag di dati**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d423-116"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>0x40</dt></span></span> </dl>                        | <span data-ttu-id="6d423-117">I dati non sono elaborati ma non sono stati completamente elaborati.</span><span class="sxs-lookup"><span data-stu-id="6d423-117">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="6d423-118"><dt>**WINBIO \_ FLAG di dati \_ \_ elaborati**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="6d423-118"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>0x80</dt></span></span> </dl>                                 | <span data-ttu-id="6d423-119">I dati sono stati elaborati.</span><span class="sxs-lookup"><span data-stu-id="6d423-119">The data has been processed.</span></span><br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="6d423-120"><dt>**WINBIO \_ Maschera di opzione del flag di dati \_ \_ \_ \_ presente**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="6d423-120"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="6d423-121">Maschera del flag.</span><span class="sxs-lookup"><span data-stu-id="6d423-121">The flag mask.</span></span> <span data-ttu-id="6d423-122">Questo valore è sempre uno (1).</span><span class="sxs-lookup"><span data-stu-id="6d423-122">This value is always one (1).</span></span><br/>                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="6d423-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d423-123">Requirements</span></span>



| <span data-ttu-id="6d423-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d423-124">Requirement</span></span> | <span data-ttu-id="6d423-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6d423-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d423-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d423-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6d423-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6d423-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6d423-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d423-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6d423-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d423-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6d423-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d423-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d423-131"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d423-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d423-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d423-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d423-133">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="6d423-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





