---
title: Costanti WINBIO_IRIS (tipi WinBio \_ . h)
description: Specificare i tipi per il riconoscimento Iris.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477489"
---
# <a name="winbio_iris-constants"></a><span data-ttu-id="9bddf-103">\_Costanti Iris WINBIO</span><span class="sxs-lookup"><span data-stu-id="9bddf-103">WINBIO\_IRIS Constants</span></span>

<span data-ttu-id="9bddf-104">Le costanti seguenti sono valori **dei \_ \_ SOTTOtipi biometrici WINBIO** che possono essere usati per specificare i tipi per il riconoscimento Iris oltre ANSI gli inci 379-2004: "formato di interscambio immagini Iris", che non definisce alcun valore di occhio sinistro/destro:</span><span class="sxs-lookup"><span data-stu-id="9bddf-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the types for iris recognition beyond ANSI INCITS 379-2004: "Iris Image Interchange Format", which does not define any left/right eye values:</span></span>



| <span data-ttu-id="9bddf-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="9bddf-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="9bddf-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bddf-106">Description</span></span>                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <span data-ttu-id="9bddf-107"><dt> **\_ Tipo Iris \_ WINBIO \_ sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-107"><dt>**WINBIO\_IRIS\_TYPE\_UNKNOWN** </dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9bddf-108">Il tipo di Iris è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9bddf-108">The iris type is unknown.</span></span> <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <span data-ttu-id="9bddf-109"><dt> **WINBIO \_ Iris \_ Left- \_ Eye**</dt> <dt>0xf5</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-109"><dt>**WINBIO\_IRIS\_LEFT\_EYE** </dt> <dt>0xF5 </dt></span></span> </dl>                               | <span data-ttu-id="9bddf-110">Il tipo Iris è l'occhio sinistro.</span><span class="sxs-lookup"><span data-stu-id="9bddf-110">The iris type is the left eye.</span></span> <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <span data-ttu-id="9bddf-111"><dt> **WINBIO \_ Iris \_ a \_ destra**</dt> <dt>0XF6</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-111"><dt>**WINBIO\_IRIS\_RIGHT\_EYE** </dt> <dt>0xF6 </dt></span></span> </dl>                            | <span data-ttu-id="9bddf-112">Il tipo Iris è l'occhio destro.</span><span class="sxs-lookup"><span data-stu-id="9bddf-112">The iris type is the right eye.</span></span> <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <span data-ttu-id="9bddf-113"><dt>**WINBIO \_ IRIS non \_ specificato \_ POS \_ 01**</dt> <dt>0xf7</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-113"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_01**</dt> <dt>0xF7</dt></span></span> </dl>    | <span data-ttu-id="9bddf-114">Sottotipo associato a un primo modello utente quando solo un occhio è la cornice della fotocamera e non può essere determinato se è l'occhio sinistro o destro dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9bddf-114">Subtype associated with a user s first template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <span data-ttu-id="9bddf-115"><dt> **WINBIO \_ Iris non \_ specificato \_ POS \_ 02**</dt> <dt>0xF8</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-115"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_02** </dt> <dt>0xF8</dt></span></span> </dl> | <span data-ttu-id="9bddf-116">Sottotipo associato a un secondo modello utente quando solo un occhio è il fotogramma della fotocamera e non può essere determinato se è l'occhio sinistro o destro dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9bddf-116">Subtype associated with a user s second template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <span data-ttu-id="9bddf-117"><dt> **WINBIO \_ Iris \_ entrambi \_ gli occhi**</dt> <dt>0xF9</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-117"><dt>**WINBIO\_IRIS\_BOTH\_EYES** </dt> <dt>0xF9</dt></span></span> </dl>                             | <span data-ttu-id="9bddf-118">Il tipo Iris è entrambi gli occhi.</span><span class="sxs-lookup"><span data-stu-id="9bddf-118">The iris type is both eyes.</span></span> <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <span data-ttu-id="9bddf-119"><dt> **WINBIO \_ Iris \_ \_ occhio**</dt> <dt>0xFA</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-119"><dt>**WINBIO\_IRIS\_EITHER\_EYE** </dt> <dt>0xFA</dt></span></span> </dl>                          | <span data-ttu-id="9bddf-120">Il tipo di Iris è Eye.</span><span class="sxs-lookup"><span data-stu-id="9bddf-120">The iris type is either eye.</span></span> <br/>                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="9bddf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bddf-121">Requirements</span></span>



| <span data-ttu-id="9bddf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bddf-122">Requirement</span></span> | <span data-ttu-id="9bddf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9bddf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bddf-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bddf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9bddf-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9bddf-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9bddf-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bddf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9bddf-127">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="9bddf-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9bddf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bddf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bddf-129"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bddf-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





