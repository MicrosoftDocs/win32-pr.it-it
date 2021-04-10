---
title: Costanti WINBIO_ORIENTATION (tipi WinBio \_ . h)
description: Le costanti seguenti specificano i possibili orientamenti della fotocamera che il componente del sensore specifica come obbligatorio.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874610"
---
# <a name="winbio_orientation-constants"></a><span data-ttu-id="70aa2-103">\_Costanti di orientamento WINBIO</span><span class="sxs-lookup"><span data-stu-id="70aa2-103">WINBIO\_ORIENTATION Constants</span></span>

<span data-ttu-id="70aa2-104">Le costanti seguenti specificano i possibili orientamenti della fotocamera che il componente del sensore specifica come obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="70aa2-104">The following constants specify the possible camera orientations that the sensor component specifies as mandatory.</span></span>



| <span data-ttu-id="70aa2-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="70aa2-105">Constant/value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="70aa2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70aa2-106">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <span data-ttu-id="70aa2-107"><dt>**WINBIO \_ ORIENTAMENTO non \_ specificato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70aa2-107"><dt>**WINBIO\_ORIENTATION\_UNSPECIFIED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="70aa2-108">Non è stato specificato un orientamento obbligatorio per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="70aa2-108">A mandatory orientation for the camera is not specified.</span></span><br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <span data-ttu-id="70aa2-109"><dt>**WINBIO \_ ORIENTAMENTO \_ orizzontale**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="70aa2-109"><dt>**WINBIO\_ORIENTATION\_LANDSCAPE**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="70aa2-110">L'orientamento orizzontale è obbligatorio per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="70aa2-110">The landscape orientation is required for the camera.</span></span><br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <span data-ttu-id="70aa2-111"><dt>**WINBIO \_ \_Verticale orientamento**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="70aa2-111"><dt>**WINBIO\_ORIENTATION\_PORTRAIT**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="70aa2-112">L'orientamento verticale è obbligatorio per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="70aa2-112">The portrait orientation is required for the camera.</span></span><br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <span data-ttu-id="70aa2-113"><dt>**WINBIO \_ ORIENTAMENTO \_**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="70aa2-113"><dt>**WINBIO\_ORIENTATION\_ANY**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="70aa2-114">Qualsiasi orientamento è consentito per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="70aa2-114">Any orientation is permitted for the camera.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="70aa2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70aa2-115">Requirements</span></span>



| <span data-ttu-id="70aa2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="70aa2-116">Requirement</span></span> | <span data-ttu-id="70aa2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="70aa2-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70aa2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70aa2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70aa2-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="70aa2-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="70aa2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70aa2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70aa2-121">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="70aa2-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="70aa2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70aa2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="70aa2-123"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="70aa2-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70aa2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70aa2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70aa2-125">**\_informazioni sul \_ sensore \_ esteso WINBIO**</span><span class="sxs-lookup"><span data-stu-id="70aa2-125">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





