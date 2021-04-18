---
title: Enumerazione WMT_RIGHTS (wmdrmsdk. h)
description: Definisce i diritti che possono essere specificati in una licenza DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- Formato Windows Media enumerazione WMT_RIGHTS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324048"
---
# <a name="wmt_rights-enumeration"></a><span data-ttu-id="78b37-105">\_Enumerazione dei diritti WMT</span><span class="sxs-lookup"><span data-stu-id="78b37-105">WMT\_RIGHTS enumeration</span></span>

<span data-ttu-id="78b37-106">Il tipo di enumerazione **\_ dei diritti WMT** definisce i diritti che possono essere specificati in una licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="78b37-106">The **WMT\_RIGHTS** enumeration type defines the rights that may be specified in a DRM license.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b37-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78b37-107">Syntax</span></span>


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a><span data-ttu-id="78b37-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="78b37-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="78b37-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT \_ riproduzione a destra \_**</span><span class="sxs-lookup"><span data-stu-id="78b37-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT\_RIGHT\_PLAYBACK**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-110">Specifica il diritto di riprodurre il contenuto senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="78b37-110">Specifies the right to play content without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="78b37-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT \_ \_ Copia \_ a destra \_ nel \_ dispositivo non SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="78b37-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-112">Specifica il diritto di copiare il contenuto in un dispositivo non conforme a Secure Digital Music Initiative (SDMI).</span><span class="sxs-lookup"><span data-stu-id="78b37-112">Specifies the right to copy content to a device not compliant with the Secure Digital Music Initiative (SDMI).</span></span>

</dd> <dt>

<span data-ttu-id="78b37-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT \_ \_ Copia \_ a destra su \_ CD**</span><span class="sxs-lookup"><span data-stu-id="78b37-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT\_RIGHT\_COPY\_TO\_CD**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-114">Specifica il diritto di copiare il contenuto in un CD.</span><span class="sxs-lookup"><span data-stu-id="78b37-114">Specifies the right to copy content to a CD.</span></span>

</dd> <dt>

<span data-ttu-id="78b37-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT \_ \_ Copia \_ a destra \_ nel \_ dispositivo SDMI**</span><span class="sxs-lookup"><span data-stu-id="78b37-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-116">Specifica il diritto di copiare il contenuto in un dispositivo conforme a SDMI.</span><span class="sxs-lookup"><span data-stu-id="78b37-116">Specifies the right to copy content to a device compliant with the SDMI.</span></span>

</dd> <dt>

<span data-ttu-id="78b37-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ giusto \_ una \_ volta**</span><span class="sxs-lookup"><span data-stu-id="78b37-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT\_RIGHT\_ONE\_TIME**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-118">Specifica il diritto di riprodurre il contenuto solo una volta.</span><span class="sxs-lookup"><span data-stu-id="78b37-118">Specifies the right to play content one time only.</span></span>

</dd> <dt>

<span data-ttu-id="78b37-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ right \_ Salva \_ flusso \_ protetto**</span><span class="sxs-lookup"><span data-stu-id="78b37-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT\_RIGHT\_SAVE\_STREAM\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-120">Specifica il diritto di salvare il contenuto da un server.</span><span class="sxs-lookup"><span data-stu-id="78b37-120">Specifies the right to save content from a server.</span></span>

</dd> <dt>

<span data-ttu-id="78b37-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT \_ copia a destra \_**</span><span class="sxs-lookup"><span data-stu-id="78b37-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT\_RIGHT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-122">Specifica il diritto di copiare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="78b37-122">Specifies the right to copy content.</span></span> <span data-ttu-id="78b37-123">Windows Media DRM 10 regola i dispositivi ai quali è possibile copiare il contenuto usando i livelli di protezione dell'output (OPLs).</span><span class="sxs-lookup"><span data-stu-id="78b37-123">Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).</span></span>

</dd> <dt>

<span data-ttu-id="78b37-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ right \_ collaborative \_ Play**</span><span class="sxs-lookup"><span data-stu-id="78b37-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT\_RIGHT\_COLLABORATIVE\_PLAY**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-125">Specifica il diritto di riprodurre il contenuto come parte di uno scenario online in cui più partecipanti possono contribuire con i brani della raccolta a una playlist condivisa.</span><span class="sxs-lookup"><span data-stu-id="78b37-125">Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.</span></span>

</dd> <dt>

<span data-ttu-id="78b37-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_trigger WMT Right \_ SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="78b37-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT\_RIGHT\_SDMI\_TRIGGER**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-127">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="78b37-127">Reserved for future use.</span></span> <span data-ttu-id="78b37-128">Non usare.</span><span class="sxs-lookup"><span data-stu-id="78b37-128">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="78b37-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ right \_ SDMI \_ NOMORECOPIES**</span><span class="sxs-lookup"><span data-stu-id="78b37-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT\_RIGHT\_SDMI\_NOMORECOPIES**</span></span>
</dt> <dd>

<span data-ttu-id="78b37-130">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="78b37-130">Reserved for future use.</span></span> <span data-ttu-id="78b37-131">Non usare.</span><span class="sxs-lookup"><span data-stu-id="78b37-131">Do not use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78b37-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="78b37-132">Remarks</span></span>

<span data-ttu-id="78b37-133">Questi valori sono flag di bit, quindi uno o più possono essere impostati combinando questi valori con **l'operatore OR** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="78b37-133">These values are bit flags, so one or more can be set by combining them with the bitwise **OR** operator.</span></span>

<span data-ttu-id="78b37-134">Quando si usa Windows Media DRM 10 **, WMT \_ right \_ copy \_ to \_ non \_ SDMI \_ Device**, **WMT \_ right \_ copy \_ to \_ SDMI \_ Device** e **WMT \_ right \_ copy \_ to \_ CD** sono sostituiti da **WMT \_ right \_ Copy**.</span><span class="sxs-lookup"><span data-stu-id="78b37-134">When using Windows Media DRM 10, **WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**, **WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**, and **WMT\_RIGHT\_COPY\_TO\_CD** are superseded by **WMT\_RIGHT\_COPY**.</span></span> <span data-ttu-id="78b37-135">Le limitazioni nei dispositivi in cui è possibile copiare il contenuto vengono specificate usando i livelli di protezione dell'output (OPLs).</span><span class="sxs-lookup"><span data-stu-id="78b37-135">Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).</span></span>

## <a name="requirements"></a><span data-ttu-id="78b37-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78b37-136">Requirements</span></span>



| <span data-ttu-id="78b37-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="78b37-137">Requirement</span></span> | <span data-ttu-id="78b37-138">Valore</span><span class="sxs-lookup"><span data-stu-id="78b37-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78b37-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78b37-139">Header</span></span><br/> | <dl> <span data-ttu-id="78b37-140"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="78b37-140"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78b37-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78b37-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b37-142">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="78b37-142">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





