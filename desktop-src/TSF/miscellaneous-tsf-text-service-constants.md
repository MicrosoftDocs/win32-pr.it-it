---
title: Costanti del servizio di testo TSF varie (Ctffunc. h)
description: Con i servizi di testo vengono usati i valori seguenti.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302245"
---
# <a name="miscellaneous-tsf-text-service-constants"></a><span data-ttu-id="dce5e-103">Costanti del servizio di testo TSF varie</span><span class="sxs-lookup"><span data-stu-id="dce5e-103">Miscellaneous TSF Text Service Constants</span></span>

<span data-ttu-id="dce5e-104">Con i servizi di testo vengono usati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dce5e-104">The following values are used with text services.</span></span>



| <span data-ttu-id="dce5e-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="dce5e-105">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="dce5e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dce5e-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <span data-ttu-id="dce5e-107"><dt>**Tf \_**</dt> <dt>0x00000001</dt> MENUREADY</span><span class="sxs-lookup"><span data-stu-id="dce5e-107"><dt>**TF\_MENUREADY**</dt> <dt>0x00000001</dt></span></span> </dl>                                                | <span data-ttu-id="dce5e-108">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="dce5e-108">Not currently used.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <span data-ttu-id="dce5e-109"><dt>**Tf \_ PROPUI \_ stato \_ SAVETOFILE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="dce5e-109"><dt>**TF\_PROPUI\_STATUS\_SAVETOFILE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="dce5e-110">La proprietà può essere serializzata.</span><span class="sxs-lookup"><span data-stu-id="dce5e-110">The property can be serialized.</span></span> <span data-ttu-id="dce5e-111">Se questo valore non è presente, la proprietà non può essere serializzata.</span><span class="sxs-lookup"><span data-stu-id="dce5e-111">If this value is not present, the property cannot be serialized.</span></span> <span data-ttu-id="dce5e-112">Questo valore viene usato con [ITfFnPropertyUIStatus:: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) e [ITfFnPropertyUIStatus:: sestatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span><span class="sxs-lookup"><span data-stu-id="dce5e-112">This value is used with [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) and [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dce5e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dce5e-113">Requirements</span></span>



| <span data-ttu-id="dce5e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dce5e-114">Requirement</span></span> | <span data-ttu-id="dce5e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="dce5e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce5e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce5e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dce5e-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dce5e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dce5e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dce5e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dce5e-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dce5e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dce5e-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="dce5e-120">Redistributable</span></span><br/>          | <span data-ttu-id="dce5e-121">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dce5e-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="dce5e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dce5e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce5e-123"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="dce5e-123"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="dce5e-124">IDL</span><span class="sxs-lookup"><span data-stu-id="dce5e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dce5e-125"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dce5e-125"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce5e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dce5e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce5e-127">ITfFnPropertyUIStatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="dce5e-127">ITfFnPropertyUIStatus::GetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[<span data-ttu-id="dce5e-128">ITfFnPropertyUIStatus:: sestatus</span><span class="sxs-lookup"><span data-stu-id="dce5e-128">ITfFnPropertyUIStatus::SetStatus</span></span>](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





