---
title: Struttura WINBIO_UNIT_SCHEMA ( \_ tipi WINBIO. h)
description: Descrive le funzionalità di un'unità biometrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- Struttura di WINBIO_UNIT_SCHEMA Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_UNIT_SCHEMA
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964907"
---
# <a name="winbio_unit_schema-structure"></a><span data-ttu-id="62d62-105">\_ \_ Struttura dello schema dell'unità WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-105">WINBIO\_UNIT\_SCHEMA structure</span></span>

<span data-ttu-id="62d62-106">La **struttura \_ \_ dello schema dell'unità WINBIO** descrive le funzionalità di un'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-106">The **WINBIO\_UNIT\_SCHEMA** structure describes the capabilities of a biometric unit.</span></span> <span data-ttu-id="62d62-107">Viene usato dalla funzione [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .</span><span class="sxs-lookup"><span data-stu-id="62d62-107">It is used by the [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62d62-108">Syntax</span></span>


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="62d62-109">Members</span><span class="sxs-lookup"><span data-stu-id="62d62-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="62d62-110">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="62d62-110">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-111">Valore che identifica l'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-111">A value that identifies the biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="62d62-112">**PoolType**</span><span class="sxs-lookup"><span data-stu-id="62d62-112">**PoolType**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-113">Valore **ULONG** che specifica il tipo di unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-113">A **ULONG** value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="62d62-114">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="62d62-114">This can be one of the following values:</span></span>



| <span data-ttu-id="62d62-115">Valore</span><span class="sxs-lookup"><span data-stu-id="62d62-115">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="62d62-116">Significato</span><span class="sxs-lookup"><span data-stu-id="62d62-116">Meaning</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="62d62-117"><dt>**\_pool WINBIO \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="62d62-117"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="62d62-118">Tipo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="62d62-118">The type is unknown.</span></span><br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="62d62-119"><dt>**\_sistema pool \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="62d62-119"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>    | <span data-ttu-id="62d62-120">La sessione si connette a una raccolta condivisa di unità biometriche gestite dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="62d62-120">The session connects to a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="62d62-121"><dt>**\_pool WINBIO \_ privato**</dt></span><span class="sxs-lookup"><span data-stu-id="62d62-121"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="62d62-122">La sessione si connette a una raccolta di unità biometriche gestite dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="62d62-122">The session connects to a collection of biometric units that are managed by the caller.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="62d62-123">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="62d62-123">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-124">Valore che specifica il tipo di unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-124">A value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="62d62-125">Attualmente è supportata solo l' **\_ \_ impronta digitale di tipo WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="62d62-125">Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="62d62-126">**SensorSubType**</span><span class="sxs-lookup"><span data-stu-id="62d62-126">**SensorSubType**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-127">Sottotipo di sensore definito per il tipo di biometria specificato dal membro **BiometricFactor** .</span><span class="sxs-lookup"><span data-stu-id="62d62-127">A sensor subtype defined for the biometric type specified by the **BiometricFactor** member.</span></span> <span data-ttu-id="62d62-128">Attualmente sono supportati solo i tipi di impronta digitale (**WINBIO \_ tipo \_ impronta digitale**).</span><span class="sxs-lookup"><span data-stu-id="62d62-128">Only fingerprint types (**WINBIO\_TYPE\_FINGERPRINT**) are currently supported.</span></span> <span data-ttu-id="62d62-129">Per le impronte digitali sono attualmente definiti i sottotipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="62d62-129">The following subtypes are currently defined for fingerprints:</span></span>

-   <span data-ttu-id="62d62-130">sottotipo del \_ sensore WINBIO \_ \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="62d62-130">WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="62d62-131">\_scorrimento del \_ sottotipo di sensore FP \_ \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-131">WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE</span></span>
-   <span data-ttu-id="62d62-132">\_tocco del \_ sottotipo del sensore FP \_ \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-132">WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH</span></span>

</dd> <dt>

<span data-ttu-id="62d62-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="62d62-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-134">Maschera di maschera delle funzionalità del sensore biometrico.</span><span class="sxs-lookup"><span data-stu-id="62d62-134">A bitmask of the biometric sensor capabilities.</span></span> <span data-ttu-id="62d62-135">Può trattarsi di un **or** bit per bit dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="62d62-135">This can be a bitwise **OR** of the following values:</span></span>

-   <span data-ttu-id="62d62-136">\_sensore funzionalità \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-136">WINBIO\_CAPABILITY\_SENSOR</span></span>
-   <span data-ttu-id="62d62-137">\_corrispondenza funzionalità \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-137">WINBIO\_CAPABILITY\_MATCHING</span></span>
-   <span data-ttu-id="62d62-138">\_database funzionalità \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-138">WINBIO\_CAPABILITY\_DATABASE</span></span>
-   <span data-ttu-id="62d62-139">\_elaborazione della funzionalità WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="62d62-139">WINBIO\_CAPABILITY\_PROCESSING</span></span>
-   <span data-ttu-id="62d62-140">\_crittografia funzionalità \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-140">WINBIO\_CAPABILITY\_ENCRYPTION</span></span>
-   <span data-ttu-id="62d62-141">\_navigazione della funzionalità WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="62d62-141">WINBIO\_CAPABILITY\_NAVIGATION</span></span>
-   <span data-ttu-id="62d62-142">\_indicatore funzionalità \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-142">WINBIO\_CAPABILITY\_INDICATOR</span></span>
-   <span data-ttu-id="62d62-143">\_ \_ sensore virtuale funzionalità \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="62d62-143">WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR</span></span>
    > [!Note]  
    > <span data-ttu-id="62d62-144">La costante del **\_ \_ \_ sensore virtuale della funzionalità WINBIO** si applica solo a Windows 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="62d62-144">The **WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR** constant applies only for Windows 10 and later.</span></span>

     

</dd> <dt>

<span data-ttu-id="62d62-145">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="62d62-145">**DeviceInstanceId**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-146">Valore stringa che contiene l'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62d62-146">A string value that contains the device ID.</span></span> <span data-ttu-id="62d62-147">La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="62d62-147">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="62d62-148">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="62d62-148">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-149">Valore stringa che contiene una descrizione dell'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-149">A string value that contains a description of the biometric unit.</span></span> <span data-ttu-id="62d62-150">La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="62d62-150">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="62d62-151">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="62d62-151">**Manufacturer**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-152">Valore stringa che contiene il nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="62d62-152">A string value that contains the name of the manufacturer.</span></span> <span data-ttu-id="62d62-153">La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="62d62-153">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="62d62-154">**Modello**</span><span class="sxs-lookup"><span data-stu-id="62d62-154">**Model**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-155">Valore stringa che contiene il numero di modello dell'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-155">A string value that contains the model number of the biometric unit.</span></span> <span data-ttu-id="62d62-156">La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="62d62-156">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="62d62-157">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="62d62-157">**SerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-158">Stringa Unicode con terminazione **null** che contiene il numero di serie dell'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-158">A **NULL**-terminated Unicode string that contains the serial number of the biometric unit.</span></span> <span data-ttu-id="62d62-159">La stringa può contenere fino a 256 caratteri Unicode, incluso un carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="62d62-159">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="62d62-160">**FirmwareVersion**</span><span class="sxs-lookup"><span data-stu-id="62d62-160">**FirmwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="62d62-161">Struttura [**di \_ versione di WINBIO**](winbio-version.md) che contiene i numeri di versione principale e secondaria per l'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="62d62-161">A [**WINBIO\_VERSION**](winbio-version.md) structure that contains the major and minor version numbers for the biometric unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62d62-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62d62-162">Requirements</span></span>



| <span data-ttu-id="62d62-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="62d62-163">Requirement</span></span> | <span data-ttu-id="62d62-164">Valore</span><span class="sxs-lookup"><span data-stu-id="62d62-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d62-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62d62-165">Minimum supported client</span></span><br/> | <span data-ttu-id="62d62-166">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="62d62-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="62d62-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62d62-167">Minimum supported server</span></span><br/> | <span data-ttu-id="62d62-168">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="62d62-168">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="62d62-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62d62-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="62d62-170"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62d62-170"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62d62-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62d62-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d62-172">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="62d62-172">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="62d62-173">**WinBioEnumBiometricUnits**</span><span class="sxs-lookup"><span data-stu-id="62d62-173">**WinBioEnumBiometricUnits**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





