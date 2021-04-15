---
title: Struttura WINBIO_EXTENDED_ENROLLMENT_PARAMETERS (WinBio \_ Adapter. h)
description: Contiene informazioni aggiuntive necessarie per la creazione di un modello di registrazione da un adattatore del motore.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- Struttura di WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475665"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a><span data-ttu-id="3780c-105">WINBIO \_ \_ struttura dei parametri di registrazione estesa \_</span><span class="sxs-lookup"><span data-stu-id="3780c-105">WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS structure</span></span>

<span data-ttu-id="3780c-106">La struttura dei **\_ \_ \_ parametri di registrazione estesa WINBIO** contiene informazioni aggiuntive necessarie a un adattatore del motore per creare un modello di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3780c-106">The **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure contains additional information that an engine adapter needs to create an enrollment template.</span></span>

## <a name="syntax"></a><span data-ttu-id="3780c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3780c-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="3780c-108">Members</span><span class="sxs-lookup"><span data-stu-id="3780c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3780c-109">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="3780c-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3780c-110">Dimensioni (in byte) della struttura dei **\_ \_ \_ parametri di registrazione estesa WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="3780c-110">The size (in bytes) of the **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="3780c-111">**Sottofattore**</span><span class="sxs-lookup"><span data-stu-id="3780c-111">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="3780c-112">Uno dei valori [**\_ \_ costanti del SOTTOtipo biometrico WINBIO**](winbio-biometric-subtype-constants.md) che fornisce informazioni aggiuntive sulla registrazione.</span><span class="sxs-lookup"><span data-stu-id="3780c-112">One of the [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md) values that provides additional information about the enrollment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3780c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3780c-113">Remarks</span></span>

<span data-ttu-id="3780c-114">Il Windows Biometric Framework passa questa struttura al metodo [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante un'operazione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3780c-114">The Windows Biometric Framework passes this structure to the [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) method during an enrollment operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3780c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3780c-115">Requirements</span></span>



| <span data-ttu-id="3780c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3780c-116">Requirement</span></span> | <span data-ttu-id="3780c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3780c-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3780c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3780c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3780c-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3780c-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="3780c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3780c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3780c-121">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="3780c-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="3780c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3780c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3780c-123"><dt>WinBio \_ Adapter. h (include WinBio \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3780c-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





