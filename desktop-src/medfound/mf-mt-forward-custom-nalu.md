---
description: Specifica che i tipi di unità del livello di astrazione della rete (NAL) devono essere trasmessi negli esempi di output dal decodificatore.
ms.assetid: 2A1D8629-EB66-4F72-9AD7-93123D941BB0
title: Attributo MF_MT_FORWARD_CUSTOM_NALU (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a318523f52ab7d65450c4c2f35b7bfbf63d5f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529947"
---
# <a name="mf_mt_forward_custom_nalu-attribute"></a><span data-ttu-id="ae203-103">\_ \_ \_ Attributo Nalu personalizzato MF mt in futuro \_</span><span class="sxs-lookup"><span data-stu-id="ae203-103">MF\_MT\_FORWARD\_CUSTOM\_NALU attribute</span></span>

<span data-ttu-id="ae203-104">Specifica che i tipi di unità del livello di astrazione della rete (NAL) devono essere trasmessi negli esempi di output dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="ae203-104">Specifies that network abstraction layer (NAL) unit types should be forwarded on output samples by the decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae203-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ae203-105">Data type</span></span>

<span data-ttu-id="ae203-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ae203-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ae203-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae203-107">Remarks</span></span>

<span data-ttu-id="ae203-108">Se il decodificatore analizza un NALU, non verrà trasmesso.</span><span class="sxs-lookup"><span data-stu-id="ae203-108">If the decoder parses a NALU then it will not be forwarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae203-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae203-109">Requirements</span></span>



| <span data-ttu-id="ae203-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae203-110">Requirement</span></span> | <span data-ttu-id="ae203-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ae203-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae203-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae203-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ae203-113">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae203-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ae203-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae203-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ae203-115">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="ae203-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ae203-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae203-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae203-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae203-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




