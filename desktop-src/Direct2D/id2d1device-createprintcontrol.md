---
title: Metodi ID2D1Device CreatePrintControl (D2d1 \_ 1. h)
description: Crea un oggetto ID2D1PrintControl che converte le primitive Direct2D archiviate in ID2D1CommandList in una rappresentazione di pagina fissa. Il sottosistema di stampa usa quindi le primitive.
ms.assetid: C8860AEE-807A-435E-9F44-B50545320EDA
keywords:
- Metodo CreatePrintControl Direct2D
topic_type:
- apiref
api_location:
- d2d1_1.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ec8705d73f40fc967b3247aaf81caebcade47b02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325090"
---
# <a name="id2d1devicecreateprintcontrol-methods"></a><span data-ttu-id="9620a-105">Metodi ID2D1Device:: CreatePrintControl</span><span class="sxs-lookup"><span data-stu-id="9620a-105">ID2D1Device::CreatePrintControl methods</span></span>

<span data-ttu-id="9620a-106">Crea un oggetto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) che converte le primitive [Direct2D](/windows/desktop/direct2d/direct2d-portal) archiviate in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) in una rappresentazione di pagina fissa.</span><span class="sxs-lookup"><span data-stu-id="9620a-106">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="9620a-107">Il sottosistema di stampa usa quindi le primitive.</span><span class="sxs-lookup"><span data-stu-id="9620a-107">The print sub-system then consumes the primitives.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9620a-108">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="9620a-108">Overload list</span></span>



| <span data-ttu-id="9620a-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="9620a-109">Method</span></span>                                                                                                                                                                           | <span data-ttu-id="9620a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9620a-110">Description</span></span>                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9620a-111">[**CreatePrintControl ( \* proprietà del controllo di stampa IWICImagingFactory, IPrintDocumentPackageTarget \* , d2d1 \_ \_ \_ \* , ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="9620a-111">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES\*, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span></span> | <span data-ttu-id="9620a-112">Crea un oggetto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) che converte le primitive [Direct2D](/windows/desktop/direct2d/direct2d-portal) archiviate in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) in una rappresentazione di pagina fissa.</span><span class="sxs-lookup"><span data-stu-id="9620a-112">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="9620a-113">Il sottosistema di stampa usa quindi le primitive.</span><span class="sxs-lookup"><span data-stu-id="9620a-113">The print sub-system then consumes the primitives.</span></span><br/> |
| <span data-ttu-id="9620a-114">[**CreatePrintControl ( \* proprietà del controllo di stampa IWICImagingFactory, IPrintDocumentPackageTarget \* , d2d1 \_ \_ \_&, ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="9620a-114">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES&, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span></span>    | <span data-ttu-id="9620a-115">Crea un oggetto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) che converte le primitive [Direct2D](/windows/desktop/direct2d/direct2d-portal) archiviate in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) in una rappresentazione di pagina fissa.</span><span class="sxs-lookup"><span data-stu-id="9620a-115">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="9620a-116">Il sottosistema di stampa usa quindi le primitive.</span><span class="sxs-lookup"><span data-stu-id="9620a-116">The print sub-system then consumes the primitives.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9620a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9620a-117">Requirements</span></span>



| <span data-ttu-id="9620a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9620a-118">Requirement</span></span> | <span data-ttu-id="9620a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9620a-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9620a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9620a-120">Header</span></span><br/> | <dl> <span data-ttu-id="9620a-121"><dt>D2d1 \_ 1. h</dt></span><span class="sxs-lookup"><span data-stu-id="9620a-121"><dt>D2d1\_1.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9620a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9620a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9620a-123">**ID2D1Device**</span><span class="sxs-lookup"><span data-stu-id="9620a-123">**ID2D1Device**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
</dt> </dl>

<span data-ttu-id="9620a-124">�</span><span class="sxs-lookup"><span data-stu-id="9620a-124">�</span></span>

<span data-ttu-id="9620a-125">�</span><span class="sxs-lookup"><span data-stu-id="9620a-125">�</span></span>
