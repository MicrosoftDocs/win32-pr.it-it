---
title: Costanti WINBIO_PRESENCE_CHANGE (tipi WinBio \_ . h)
description: Vengono descritti i tipi di modifiche che possono verificarsi quando il Windows Biometric Framework monitora la presenza di singoli utenti.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047964"
---
# <a name="winbio_presence_change-constants"></a><span data-ttu-id="59277-103">Costanti di modifica della \_ presenza WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="59277-103">WINBIO\_PRESENCE\_CHANGE Constants</span></span>

<span data-ttu-id="59277-104">Vengono descritti i tipi di modifiche che possono verificarsi quando il Windows Biometric Framework monitora la presenza di singoli utenti.</span><span class="sxs-lookup"><span data-stu-id="59277-104">Describes the types of changes that can occur when the Windows Biometric Framework monitors the presence of individuals.</span></span>



| <span data-ttu-id="59277-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="59277-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="59277-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59277-106">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <span data-ttu-id="59277-107"><dt>**WINBIO \_ Tipo di modifica della presenza \_ \_ \_ sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59277-107"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="59277-108">Il tipo di evento è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="59277-108">The type of event is unknown.</span></span> <span data-ttu-id="59277-109">Questo valore viene utilizzato per la struttura non inizializzata.</span><span class="sxs-lookup"><span data-stu-id="59277-109">This value is used for the uninitialized structure.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <span data-ttu-id="59277-110"><dt>**WINBIO \_ Aggiornamento del tipo di modifica della presenza- \_ \_ \_ \_ tutti**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="59277-110"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UPDATE\_ALL**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="59277-111">Fornisce informazioni su tutti i visi correnti nel frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="59277-111">Provides information about all of the faces current in the camera frame.</span></span><br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <span data-ttu-id="59277-112"><dt>**WINBIO \_ \_Arrivo del \_ tipo \_ di modifica della presenza**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="59277-112"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_ARRIVE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="59277-113">Un nuovo volto è entrato nel frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="59277-113">A new face entered the camera frame.</span></span><br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <span data-ttu-id="59277-114"><dt>**WINBIO \_ Tipo di modifica della presenza \_ \_ \_ Riconosci**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="59277-114"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_RECOGNIZE**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="59277-115">Una faccia corrisponde a un utente registrato.</span><span class="sxs-lookup"><span data-stu-id="59277-115">A face was matched to an enrolled user.</span></span><br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <span data-ttu-id="59277-116"><dt>**WINBIO \_ Tipo di modifica della presenza- \_ \_ \_ parte**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="59277-116"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_DEPART**</dt> <dt>4</dt></span></span> </dl>              | <span data-ttu-id="59277-117">Un viso rilevato in precedenza è stato fuori dal fotogramma della fotocamera per un certo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="59277-117">A previously detected face has been out of the camera frame for a period of time.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <span data-ttu-id="59277-118"><dt>**WINBIO \_ Tipo di modifica della presenza \_ \_ \_ Track**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="59277-118"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_TRACK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="59277-119">Fornisce informazioni sugli aggiornamenti sul riquadro e rifiuta i valori di dettaglio per un subset delle facce attualmente presenti nel frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="59277-119">Provides updates information about the bounding box and reject detail values for a subset of the faces that are currently in the camera frame.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="59277-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59277-120">Requirements</span></span>



| <span data-ttu-id="59277-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="59277-121">Requirement</span></span> | <span data-ttu-id="59277-122">Valore</span><span class="sxs-lookup"><span data-stu-id="59277-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59277-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59277-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59277-124">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="59277-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="59277-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59277-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59277-126">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="59277-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="59277-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59277-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="59277-128"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="59277-128"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





