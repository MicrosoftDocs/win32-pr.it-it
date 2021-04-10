---
title: Costanti WINBIO_ANSI_385_FACE (tipi WinBio \_ . h)
description: Specificare i tipi di immagine frontali per il riconoscimento facciale.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120926"
---
# <a name="winbio_ansi_385_face-constants"></a><span data-ttu-id="8c5dc-103">\_Costanti della \_ faccia ANSI 385 di WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="8c5dc-103">WINBIO\_ANSI\_385\_FACE Constants</span></span>

<span data-ttu-id="8c5dc-104">Le costanti seguenti sono valori **dei \_ \_ SOTTOtipi biometrici di WINBIO** che possono essere usati per specificare i due tipi di immagini facciali frontali come definito da ANSI incis 385-2004: "formato riconoscimento viso per interscambio dati": risoluzione completa e risoluzione bassa.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the two types of frontal face images as defined by ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": full resolution and low resolution.</span></span> <span data-ttu-id="8c5dc-105">In pratica, il Framework biometrico userà solo le immagini a risoluzione completa per il riconoscimento facciale.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-105">In practice, the biometric framework will use only full resolution images for facial recognition.</span></span>



| <span data-ttu-id="8c5dc-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="8c5dc-106">Constant/value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="8c5dc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c5dc-107">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <span data-ttu-id="8c5dc-108"><dt>**WINBIO \_ \_Tipo di \_ viso ANSI 385 \_ \_ sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c5dc-108"><dt>**WINBIO\_ANSI\_385\_FACE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="8c5dc-109">Il tipo di immagine della faccia anteriore è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-109">The frontal face image type is unknown.</span></span><br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <span data-ttu-id="8c5dc-110"><dt>**WINBIO \_ ANSI \_ 385 \_ viso \_ anteriore \_ completo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8c5dc-110"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_FULL**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="8c5dc-111">Il tipo di immagine frontale della faccia è la risoluzione completa.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-111">The frontal face image type is full resolution.</span></span><br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <span data-ttu-id="8c5dc-112"><dt>**WINBIO \_ \_ \_ \_ \_ Token anteriore del fronte ANSI 385**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c5dc-112"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_TOKEN**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="8c5dc-113">Il tipo di immagine frontale della faccia è a bassa risoluzione.</span><span class="sxs-lookup"><span data-stu-id="8c5dc-113">The frontal face image type is low resolution.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="8c5dc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c5dc-114">Requirements</span></span>



| <span data-ttu-id="8c5dc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c5dc-115">Requirement</span></span> | <span data-ttu-id="8c5dc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8c5dc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c5dc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c5dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c5dc-118">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8c5dc-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="8c5dc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c5dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c5dc-120">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8c5dc-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8c5dc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c5dc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c5dc-122"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c5dc-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





