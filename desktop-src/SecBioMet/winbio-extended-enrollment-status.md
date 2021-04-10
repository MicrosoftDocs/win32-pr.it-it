---
title: Struttura WINBIO_EXTENDED_ENROLLMENT_STATUS ( \_ tipi WINBIO. h)
description: Contiene informazioni aggiuntive sullo stato di una registrazione in corso.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- Struttura di WINBIO_EXTENDED_ENROLLMENT_STATUS Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_ENROLLMENT_STATUS
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119219"
---
# <a name="winbio_extended_enrollment_status-structure"></a><span data-ttu-id="00d84-105">WINBIO \_ \_ \_ struttura dello stato di registrazione estesa</span><span class="sxs-lookup"><span data-stu-id="00d84-105">WINBIO\_EXTENDED\_ENROLLMENT\_STATUS structure</span></span>

<span data-ttu-id="00d84-106">Contiene informazioni aggiuntive sullo stato di una registrazione in corso.</span><span class="sxs-lookup"><span data-stu-id="00d84-106">Contains additional information about the status of an enrollment that is in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d84-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00d84-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="00d84-108">Members</span><span class="sxs-lookup"><span data-stu-id="00d84-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="00d84-109">**TemplateStatus**</span><span class="sxs-lookup"><span data-stu-id="00d84-109">**TemplateStatus**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-110">Stato della raccolta di esempi per il modello di registrazione.</span><span class="sxs-lookup"><span data-stu-id="00d84-110">The status of sample collection for the enrollment template.</span></span> <span data-ttu-id="00d84-111">Per questo membro sono possibili i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="00d84-111">The following values are possible for this member.</span></span>



| <span data-ttu-id="00d84-112">Valore</span><span class="sxs-lookup"><span data-stu-id="00d84-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="00d84-113">Significato</span><span class="sxs-lookup"><span data-stu-id="00d84-113">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="00d84-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00d84-114"><dt>**S\_OK**</dt></span></span> </dl>                                                                     | <span data-ttu-id="00d84-115">La registrazione è pronta per essere salvata.</span><span class="sxs-lookup"><span data-stu-id="00d84-115">The enrollment is ready to be saved.</span></span><br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <span data-ttu-id="00d84-116"><dt>**\_operazione WINBIO E \_ non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00d84-116"><dt>**WINBIO\_E\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="00d84-117">Nessuna registrazione in corso.</span><span class="sxs-lookup"><span data-stu-id="00d84-117">No enrollment is in progress.</span></span><br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <span data-ttu-id="00d84-118"><dt>**WINBIO \_ \_ più \_ dati**</dt></span><span class="sxs-lookup"><span data-stu-id="00d84-118"><dt>**WINBIO\_I\_MORE\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="00d84-119">Per completare il modello sono necessari altri esempi.</span><span class="sxs-lookup"><span data-stu-id="00d84-119">More samples are required to complete the template.</span></span><br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <span data-ttu-id="00d84-120"><dt>**WINBIO \_ E \_ acquisizione non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00d84-120"><dt>**WINBIO\_E\_BAD\_CAPTURE**</dt></span></span> </dl>                   | <span data-ttu-id="00d84-121">L'esempio più recente non è utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="00d84-121">The most recent sample is not usable.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="00d84-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="00d84-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-123">Il motivo per cui l'esempio più recente è inutilizzabile, se il valore del membro **TemplateStatus** è **WINBIO \_ E \_ Bad \_ Capture**.</span><span class="sxs-lookup"><span data-stu-id="00d84-123">The reason that the most recent sample is unusable, if the value of the **TemplateStatus** member is **WINBIO\_E\_BAD\_CAPTURE**.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-124">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="00d84-124">**PercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-125">Stima migliore dall'adattatore del motore per la percentuale del modello completo, come valore compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="00d84-125">The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-126">**Fattore**</span><span class="sxs-lookup"><span data-stu-id="00d84-126">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-127">Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore.</span><span class="sxs-lookup"><span data-stu-id="00d84-127">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="00d84-128">Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura di [**\_ informazioni del \_ motore \_ esteso WINBIO**](winbio-extended-engine-info.md) si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="00d84-128">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-129">**Sottofattore**</span><span class="sxs-lookup"><span data-stu-id="00d84-129">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-130">Valore **del \_ \_ SOTTOtipo biometrico WINBIO** che fornisce informazioni aggiuntive sulla registrazione.</span><span class="sxs-lookup"><span data-stu-id="00d84-130">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that provides additional information about the enrollment.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-131">**Specifica**</span><span class="sxs-lookup"><span data-stu-id="00d84-131">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-132">Informazioni sullo stato di una registrazione in corso per un fattore biometrico specifico.</span><span class="sxs-lookup"><span data-stu-id="00d84-132">Information about the status of an enrollment that is in progress for a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="00d84-133">**Null**</span><span class="sxs-lookup"><span data-stu-id="00d84-133">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-134">Riservato.</span><span class="sxs-lookup"><span data-stu-id="00d84-134">Reserved.</span></span> <span data-ttu-id="00d84-135">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="00d84-135">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-136">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="00d84-136">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-137">Informazioni sullo stato di una registrazione in corso per le funzionalità facciali.</span><span class="sxs-lookup"><span data-stu-id="00d84-137">Information about the status of an enrollment that is in progress for facial features.</span></span>

<dl> <dt>

<span data-ttu-id="00d84-138">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="00d84-138">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-139">Posizione all'interno del frame della fotocamera della faccia del singolo oggetto da registrare, in pixel.</span><span class="sxs-lookup"><span data-stu-id="00d84-139">The position within the camera frame of the face of the individual to enroll, in pixels.</span></span> <span data-ttu-id="00d84-140">La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione.</span><span class="sxs-lookup"><span data-stu-id="00d84-140">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="00d84-141">Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-141">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="00d84-142">Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-142">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-143">**Distanza**</span><span class="sxs-lookup"><span data-stu-id="00d84-143">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-144">Distanza tra la posizione effettiva della faccia e la distanza focale ideale per la superficie.</span><span class="sxs-lookup"><span data-stu-id="00d84-144">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="00d84-145">Questo valore è compreso tra-100 e 100.</span><span class="sxs-lookup"><span data-stu-id="00d84-145">This value ranges from -100 to 100.</span></span> <span data-ttu-id="00d84-146">0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva della faccia è troppo distante e i valori negativi indicano che la posizione effettiva è troppo vicina.</span><span class="sxs-lookup"><span data-stu-id="00d84-146">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="00d84-147">**Impronta digitale**</span><span class="sxs-lookup"><span data-stu-id="00d84-147">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-148">Informazioni sullo stato di una registrazione in corso per i modelli di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="00d84-148">Information about the status of an enrollment that is in progress for fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="00d84-149">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="00d84-149">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-150">Numero totale di campioni necessari per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="00d84-150">The total number of samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-151">**Center**</span><span class="sxs-lookup"><span data-stu-id="00d84-151">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-152">Il numero di campioni per il centro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="00d84-152">The number of samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-153">**TopEdge**</span><span class="sxs-lookup"><span data-stu-id="00d84-153">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-154">Il numero di campioni per il bordo superiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="00d84-154">The number of samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-155">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="00d84-155">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-156">Il numero di campioni per il bordo inferiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="00d84-156">The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-157">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="00d84-157">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-158">Il numero di campioni per il bordo sinistro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="00d84-158">The number of samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-159">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="00d84-159">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-160">Il numero di campioni per il bordo destro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="00d84-160">The number of samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="00d84-161">**Iris**</span><span class="sxs-lookup"><span data-stu-id="00d84-161">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-162">Informazioni sullo stato di una registrazione in corso per i modelli Iris.</span><span class="sxs-lookup"><span data-stu-id="00d84-162">Information about the status of an enrollment that is in progress for iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="00d84-163">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="00d84-163">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-164">Posizione all'interno del frame della fotocamera di uno degli Iris del singolo oggetto da registrare, in pixel.</span><span class="sxs-lookup"><span data-stu-id="00d84-164">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="00d84-165">Se il sistema di riconoscimento Iris sta monitorando solo un occhio, questa posizione è l'iride di quell'occhio.</span><span class="sxs-lookup"><span data-stu-id="00d84-165">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="00d84-166">Se il sistema di riconoscimento Iris monitora entrambi gli occhi, ma solo un occhio si trova nel fotogramma della fotocamera, questa posizione è l'iride dell'occhio nel frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-166">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="00d84-167">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel frame della fotocamera, questa posizione è probabilmente l'iride dell'occhio destro del singolo utente.</span><span class="sxs-lookup"><span data-stu-id="00d84-167">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="00d84-168">La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione.</span><span class="sxs-lookup"><span data-stu-id="00d84-168">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="00d84-169">Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-169">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="00d84-170">Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-170">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-171">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="00d84-171">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-172">Posizione all'interno del frame della fotocamera di uno degli Iris del singolo oggetto da registrare, in pixel.</span><span class="sxs-lookup"><span data-stu-id="00d84-172">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="00d84-173">Se il sistema di riconoscimento Iris sta monitorando solo un occhio o se solo un occhio è nel frame della fotocamera, questo valore è vuoto.</span><span class="sxs-lookup"><span data-stu-id="00d84-173">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="00d84-174">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente di Iris dell'occhio sinistro del singolo utente.</span><span class="sxs-lookup"><span data-stu-id="00d84-174">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="00d84-175">La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione.</span><span class="sxs-lookup"><span data-stu-id="00d84-175">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="00d84-176">Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-176">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="00d84-177">Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-177">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-178">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="00d84-178">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-179">Posizione del centro di uno degli alunni del singolo oggetto da registrare.</span><span class="sxs-lookup"><span data-stu-id="00d84-179">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="00d84-180">Se il sistema di riconoscimento Iris sta monitorando solo un occhio, questa posizione è al centro della pupilla di quell'occhio.</span><span class="sxs-lookup"><span data-stu-id="00d84-180">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="00d84-181">Se il sistema di riconoscimento Iris monitora entrambi gli occhi, ma solo un occhio si trova nel fotogramma della fotocamera, questa posizione è al centro della pupilla dell'occhio nel frame della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="00d84-181">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="00d84-182">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente al centro della pupilla dell'occhio destro della persona.</span><span class="sxs-lookup"><span data-stu-id="00d84-182">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-183">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="00d84-183">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-184">Posizione del centro di uno degli alunni del singolo oggetto da registrare.</span><span class="sxs-lookup"><span data-stu-id="00d84-184">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="00d84-185">Se il sistema di riconoscimento Iris sta monitorando solo un occhio o se solo un occhio è nel frame della fotocamera, questo valore è vuoto.</span><span class="sxs-lookup"><span data-stu-id="00d84-185">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="00d84-186">Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente al centro della pupilla dell'occhio sinistro del singolo utente.</span><span class="sxs-lookup"><span data-stu-id="00d84-186">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="00d84-187">**Distanza**</span><span class="sxs-lookup"><span data-stu-id="00d84-187">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-188">Distanza tra la posizione effettiva dell'iride e la distanza focale ideale per l'Iris.</span><span class="sxs-lookup"><span data-stu-id="00d84-188">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="00d84-189">Questo valore è compreso tra-100 e 100.</span><span class="sxs-lookup"><span data-stu-id="00d84-189">This value ranges from -100 to 100.</span></span> <span data-ttu-id="00d84-190">0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva dell'Iris è troppo distante e i valori negativi indicano che la posizione effettiva è troppo vicina.</span><span class="sxs-lookup"><span data-stu-id="00d84-190">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="00d84-191">**Chiamata vocale**</span><span class="sxs-lookup"><span data-stu-id="00d84-191">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-192">Informazioni sullo stato di una registrazione in corso per i modelli vocali.</span><span class="sxs-lookup"><span data-stu-id="00d84-192">Information about the status of an enrollment that is in progress for voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="00d84-193">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="00d84-193">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="00d84-194">Riservato.</span><span class="sxs-lookup"><span data-stu-id="00d84-194">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00d84-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00d84-195">Requirements</span></span>



| <span data-ttu-id="00d84-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d84-196">Requirement</span></span> | <span data-ttu-id="00d84-197">Valore</span><span class="sxs-lookup"><span data-stu-id="00d84-197">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d84-198">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d84-198">Minimum supported client</span></span><br/> | <span data-ttu-id="00d84-199">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="00d84-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="00d84-200">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d84-200">Minimum supported server</span></span><br/> | <span data-ttu-id="00d84-201">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="00d84-201">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="00d84-202">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00d84-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d84-203"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="00d84-203"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





