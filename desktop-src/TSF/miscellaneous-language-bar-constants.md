---
title: Costanti della barra del linguaggio varie (Ctfutb. h)
description: Le costanti della barra del linguaggio varie impostano determinate proprietà delle barre della lingua.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400850"
---
# <a name="miscellaneous-language-bar-constants"></a><span data-ttu-id="0d4fb-103">Costanti della barra del linguaggio varie</span><span class="sxs-lookup"><span data-stu-id="0d4fb-103">Miscellaneous Language Bar Constants</span></span>

<span data-ttu-id="0d4fb-104">Le costanti della barra del linguaggio varie impostano determinate proprietà delle barre della lingua.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-104">The miscellaneous language bar constants set certain properties of language bars.</span></span>



| <span data-ttu-id="0d4fb-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="0d4fb-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="0d4fb-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d4fb-106">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <span data-ttu-id="0d4fb-107"><dt>**Tf \_ DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-107"><dt>**TF\_DTLBI\_USEPROFILEICON**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0d4fb-108">Nell'elemento barra della lingua di sistema deve essere visualizzata l'icona specificata per il profilo della lingua.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-108">The system language bar item should display the icon specified for the language profile.</span></span> <span data-ttu-id="0d4fb-109">Utilizzato nei metodi [ITfSystemDeviceTypeLangBarItem:: GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) e [ITfSystemDeviceTypeLangBarItem:: SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) .</span><span class="sxs-lookup"><span data-stu-id="0d4fb-109">Used in the [ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) and [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) methods.</span></span><br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <span data-ttu-id="0d4fb-110"><dt>**Tf \_ INVALIDMENUITEM**</dt> <dt>(uint) (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-110"><dt>**TF\_INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt></span></span> </dl>                 | <span data-ttu-id="0d4fb-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-111">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <span data-ttu-id="0d4fb-112"><dt>**Tf \_ LBI \_ BMPF \_ Vertical**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-112"><dt>**TF\_LBI\_BMPF\_VERTICAL**</dt> <dt>0x00000001</dt></span></span> </dl>         | <span data-ttu-id="0d4fb-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="0d4fb-113">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <span data-ttu-id="0d4fb-114"><dt>**Tf \_ LBI \_ desc \_ maxlen**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-114"><dt>**TF\_LBI\_DESC\_MAXLEN**</dt> <dt>32</dt></span></span> </dl>                       | <span data-ttu-id="0d4fb-115">Lunghezza, in caratteri WCHAR, del membro di struttura [tf \_ LANGBARITEMINFO. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span><span class="sxs-lookup"><span data-stu-id="0d4fb-115">Length, in WCHAR characters, of structure member [TF\_LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span></span><br/>                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="0d4fb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d4fb-116">Requirements</span></span>



| <span data-ttu-id="0d4fb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4fb-117">Requirement</span></span> | <span data-ttu-id="0d4fb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0d4fb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4fb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0d4fb-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d4fb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0d4fb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0d4fb-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d4fb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d4fb-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0d4fb-123">Redistributable</span></span><br/>          | <span data-ttu-id="0d4fb-124">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0d4fb-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="0d4fb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d4fb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d4fb-126"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d4fb-127">IDL</span><span class="sxs-lookup"><span data-stu-id="0d4fb-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d4fb-128"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fb-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d4fb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d4fb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4fb-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span><span class="sxs-lookup"><span data-stu-id="0d4fb-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[<span data-ttu-id="0d4fb-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span><span class="sxs-lookup"><span data-stu-id="0d4fb-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[<span data-ttu-id="0d4fb-132">\_LANGBARITEMINFO TF</span><span class="sxs-lookup"><span data-stu-id="0d4fb-132">TF\_LANGBARITEMINFO</span></span>](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





