---
title: Unione WINBIO_PRESENCE_PROPERTIES ( \_ tipi WINBIO. h)
description: Contiene i valori biometrici utilizzati dal Windows Biometric Framework per determinare la presenza di un singolo utente.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- API Windows Biometric Framework di WINBIO_PRESENCE_PROPERTIES Union
- API Windows Biometric Framework PWINBIO_PRESENCE_PROPERTIES puntatore Unione
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475664"
---
# <a name="winbio_presence_properties-union"></a><span data-ttu-id="8e57d-105">\_ \_ Unione proprietà presenza WINBIO</span><span class="sxs-lookup"><span data-stu-id="8e57d-105">WINBIO\_PRESENCE\_PROPERTIES union</span></span>

<span data-ttu-id="8e57d-106">Contiene i valori biometrici utilizzati dal Windows Biometric Framework per determinare la presenza di un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="8e57d-106">Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e57d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e57d-107">Syntax</span></span>


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a><span data-ttu-id="8e57d-108">Members</span><span class="sxs-lookup"><span data-stu-id="8e57d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8e57d-109">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="8e57d-109">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-110">Valori per la posizione delle funzionalità facciali usate dal Windows Biometric Framework per determinare la presenza di un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="8e57d-110">Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="8e57d-111">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="8e57d-111">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-112">Posizione all'interno del frame della fotocamera della faccia del singolo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8e57d-112">The position within the camera frame of the face of the individual, in pixels.</span></span> <span data-ttu-id="8e57d-113">La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione.</span><span class="sxs-lookup"><span data-stu-id="8e57d-113">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="8e57d-114">Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-114">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="8e57d-115">Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-115">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame .</span></span>

</dd> <dt>

<span data-ttu-id="8e57d-116">**Distanza**</span><span class="sxs-lookup"><span data-stu-id="8e57d-116">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-117">Distanza tra la posizione effettiva della faccia e la distanza focale ideale per la superficie.</span><span class="sxs-lookup"><span data-stu-id="8e57d-117">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="8e57d-118">Questo valore è compreso tra-100 e 100.</span><span class="sxs-lookup"><span data-stu-id="8e57d-118">This value ranges from -100 to 100.</span></span> <span data-ttu-id="8e57d-119">0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva della faccia è troppo distante e i valori negativi indicano che la posizione effettiva è troppo vicina.</span><span class="sxs-lookup"><span data-stu-id="8e57d-119">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8e57d-120">**Iris**</span><span class="sxs-lookup"><span data-stu-id="8e57d-120">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-121">Valori per la posizione di Iris utilizzata dall'Windows Biometric Framework per determinare la presenza di un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="8e57d-121">Values for iris location that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="8e57d-122">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8e57d-122">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-123">Posizione all'interno del frame della fotocamera di uno degli Iris del singolo oggetto da registrare, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8e57d-123">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="8e57d-124">Se il sistema di riconoscimento Iris sta monitorando solo un occhio, questa posizione è l'iride di quell'occhio.</span><span class="sxs-lookup"><span data-stu-id="8e57d-124">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="8e57d-125">Se il sistema di riconoscimento Iris monitora entrambi gli occhi, ma solo un occhio si trova nel fotogramma della fotocamera, questa posizione è l'iride dell'occhio nel frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-125">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="8e57d-126">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel frame della fotocamera, questa posizione è probabilmente l'iride dell'occhio destro del singolo utente.</span><span class="sxs-lookup"><span data-stu-id="8e57d-126">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="8e57d-127">La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione.</span><span class="sxs-lookup"><span data-stu-id="8e57d-127">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="8e57d-128">Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-128">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="8e57d-129">Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-129">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="8e57d-130">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8e57d-130">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-131">Posizione all'interno del frame della fotocamera di uno degli Iris del singolo oggetto da registrare, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8e57d-131">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="8e57d-132">Se il sistema di riconoscimento Iris sta monitorando solo un occhio o se solo un occhio è nel frame della fotocamera, questo valore è vuoto.</span><span class="sxs-lookup"><span data-stu-id="8e57d-132">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="8e57d-133">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente di Iris dell'occhio sinistro del singolo utente.</span><span class="sxs-lookup"><span data-stu-id="8e57d-133">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="8e57d-134">La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione.</span><span class="sxs-lookup"><span data-stu-id="8e57d-134">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="8e57d-135">Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-135">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="8e57d-136">Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-136">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="8e57d-137">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8e57d-137">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-138">Posizione del centro di uno degli alunni del singolo oggetto da registrare.</span><span class="sxs-lookup"><span data-stu-id="8e57d-138">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="8e57d-139">Se il sistema di riconoscimento Iris sta monitorando solo un occhio, questa posizione è al centro della pupilla di quell'occhio.</span><span class="sxs-lookup"><span data-stu-id="8e57d-139">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="8e57d-140">Se il sistema di riconoscimento Iris monitora entrambi gli occhi, ma solo un occhio si trova nel fotogramma della fotocamera, questa posizione è al centro della pupilla dell'occhio nel frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8e57d-140">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="8e57d-141">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente al centro della pupilla dell'occhio destro della persona.</span><span class="sxs-lookup"><span data-stu-id="8e57d-141">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="8e57d-142">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8e57d-142">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-143">Posizione del centro di uno degli alunni del singolo oggetto da registrare.</span><span class="sxs-lookup"><span data-stu-id="8e57d-143">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="8e57d-144">Se il sistema di riconoscimento Iris sta monitorando solo un occhio o se solo un occhio è nel frame della fotocamera, questo valore è vuoto.</span><span class="sxs-lookup"><span data-stu-id="8e57d-144">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="8e57d-145">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente al centro della pupilla dell'occhio sinistro del singolo utente.</span><span class="sxs-lookup"><span data-stu-id="8e57d-145">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="8e57d-146">**Distanza**</span><span class="sxs-lookup"><span data-stu-id="8e57d-146">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="8e57d-147">Distanza tra la posizione effettiva dell'iride e la distanza focale ideale per l'Iris.</span><span class="sxs-lookup"><span data-stu-id="8e57d-147">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="8e57d-148">Questo valore è compreso tra-100 e 100.</span><span class="sxs-lookup"><span data-stu-id="8e57d-148">This value ranges from -100 to 100.</span></span> <span data-ttu-id="8e57d-149">0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva dell'Iris è troppo distante e i valori negativi indicano che la posizione effettiva è troppo vicina.</span><span class="sxs-lookup"><span data-stu-id="8e57d-149">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e57d-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e57d-150">Requirements</span></span>



| <span data-ttu-id="8e57d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e57d-151">Requirement</span></span> | <span data-ttu-id="8e57d-152">Valore</span><span class="sxs-lookup"><span data-stu-id="8e57d-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e57d-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e57d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8e57d-154">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8e57d-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="8e57d-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e57d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8e57d-156">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8e57d-156">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="8e57d-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e57d-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e57d-158"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="8e57d-158"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





