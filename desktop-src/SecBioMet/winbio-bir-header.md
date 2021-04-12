---
title: Struttura WINBIO_BIR_HEADER ( \_ tipi WINBIO. h)
description: Contiene l'intestazione di un record di informazioni biometriche (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- Struttura di WINBIO_BIR_HEADER Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119783"
---
# <a name="winbio_bir_header-structure"></a><span data-ttu-id="34102-104">\_Struttura dell' \_ intestazione WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="34102-104">WINBIO\_BIR\_HEADER structure</span></span>

<span data-ttu-id="34102-105">La struttura dell' **\_ \_ intestazione WINBIO bir** contiene l'intestazione di un record di informazioni biometriche (Bir).</span><span class="sxs-lookup"><span data-stu-id="34102-105">The **WINBIO\_BIR\_HEADER** structure contains the header of a biometric information record (BIR).</span></span>

## <a name="syntax"></a><span data-ttu-id="34102-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34102-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a><span data-ttu-id="34102-107">Members</span><span class="sxs-lookup"><span data-stu-id="34102-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="34102-108">**ValidFields**</span><span class="sxs-lookup"><span data-stu-id="34102-108">**ValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="34102-109">Maschera di maschera che specifica i campi della struttura validi.</span><span class="sxs-lookup"><span data-stu-id="34102-109">Bitmask that specifies which fields in this structure are valid.</span></span> <span data-ttu-id="34102-110">Per altre informazioni, vedere [**\_ costanti di \_ campo WINBIO bir**](winbio-bir-field-constants.md).</span><span class="sxs-lookup"><span data-stu-id="34102-110">For more information, see [**WINBIO\_BIR\_FIELD Constants**](winbio-bir-field-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="34102-111">**HeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="34102-111">**HeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="34102-112">Costante **di \_ \_ versione di WINBIO bir** che specifica la versione dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="34102-112">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="34102-113">I numeri di versione sono valori a 8 bit, dove i quattro bit più alti specificano il numero principale e i quattro bit bassi specificano il numero di versione secondario.</span><span class="sxs-lookup"><span data-stu-id="34102-113">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="34102-114">Attualmente deve essere WINBIO \_ CBEFF \_ header \_ Version (0x11).</span><span class="sxs-lookup"><span data-stu-id="34102-114">Currently this must be WINBIO\_CBEFF\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="34102-115">**PatronHeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="34102-115">**PatronHeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="34102-116">Costante **di \_ \_ versione di WINBIO bir** che specifica la versione dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="34102-116">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="34102-117">I numeri di versione sono valori a 8 bit, dove i quattro bit più alti specificano il numero principale e i quattro bit bassi specificano il numero di versione secondario.</span><span class="sxs-lookup"><span data-stu-id="34102-117">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="34102-118">Attualmente deve essere WINBIO \_ patron \_ header \_ Version (0x11).</span><span class="sxs-lookup"><span data-stu-id="34102-118">Currently this must be WINBIO\_PATRON\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="34102-119">**Flag dataflag**</span><span class="sxs-lookup"><span data-stu-id="34102-119">**DataFlags**</span></span>
</dt> <dd>

<span data-ttu-id="34102-120">Valore che specifica il formato dei dati di intestazione.</span><span class="sxs-lookup"><span data-stu-id="34102-120">A value that specifies the format of the header data.</span></span> <span data-ttu-id="34102-121">Può trattarsi di un **or** bit per bit dei flag del livello di sicurezza e di elaborazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="34102-121">This can be a bitwise **OR** of the following security and processing level flags.</span></span> <span data-ttu-id="34102-122">Per altre informazioni, vedere [**\_ \_ \_ costanti flag di dati WINBIO bir**](winbio-bir-data-flags-constants.md).</span><span class="sxs-lookup"><span data-stu-id="34102-122">For more information, see [**WINBIO\_BIR\_DATA\_FLAGS Constants**](winbio-bir-data-flags-constants.md).</span></span>



| <span data-ttu-id="34102-123">Valore</span><span class="sxs-lookup"><span data-stu-id="34102-123">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="34102-124">Significato</span><span class="sxs-lookup"><span data-stu-id="34102-124">Meaning</span></span>                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="34102-125"><dt>**WINBIO \_ \_ \_ Privacy del flag di dati**</dt> <dt>((UCHAR) 0x02)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-125"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>((UCHAR)0x02)</dt></span></span> </dl>                                       | <span data-ttu-id="34102-126">I dati sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="34102-126">The data is encrypted.</span></span><br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="34102-127"><dt>**WINBIO \_ \_ \_ Integrità del flag di dati**</dt> <dt>((UCHAR) 0x01)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-127"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>((UCHAR)0x01)</dt></span></span> </dl>                                 | <span data-ttu-id="34102-128">I dati sono firmati digitalmente o protetti da un codice MAC (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="34102-128">The data is digitally signed or protected by a message authentication code (MAC).</span></span><br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="34102-129"><dt>**WINBIO \_ \_Flag data \_ firmato**</dt> <dt>((UCHAR) 0x04)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-129"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>((UCHAR)0x04)</dt></span></span> </dl>                                          | <span data-ttu-id="34102-130">Se vengono impostati questo flag e il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , i dati vengono firmati.</span><span class="sxs-lookup"><span data-stu-id="34102-130">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="34102-131">Se questo flag non è impostato ma è impostato il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , viene calcolato un Mac sui dati.</span><span class="sxs-lookup"><span data-stu-id="34102-131">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed over the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="34102-132"><dt>**WINBIO \_ \_Flag dati \_ RAW**</dt> <dt>((UCHAR) 0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-132"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>((UCHAR)0x20)</dt></span></span> </dl>                                                   | <span data-ttu-id="34102-133">I dati sono nel formato con cui sono stati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="34102-133">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="34102-134"><dt>**WINBIO \_ FLAG di dati \_ \_ intermedio**</dt> <dt>((UCHAR) 0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-134"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt></span></span> </dl>                        | <span data-ttu-id="34102-135">I dati non sono elaborati ma non sono stati completamente elaborati.</span><span class="sxs-lookup"><span data-stu-id="34102-135">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="34102-136"><dt>**WINBIO \_ FLAG di dati \_ \_ elaborati**</dt> <dt>((UCHAR) 0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-136"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>((UCHAR)0x80)</dt></span></span> </dl>                                 | <span data-ttu-id="34102-137">I dati sono stati elaborati.</span><span class="sxs-lookup"><span data-stu-id="34102-137">The data has been processed.</span></span><br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="34102-138"><dt>**WINBIO \_ \_Maschera di \_ opzione flag dati \_ \_ presente**</dt> <dt>((UCHAR) 0x08)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-138"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>((UCHAR)0x08)</dt></span></span> </dl> | <span data-ttu-id="34102-139">Il valore è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="34102-139">This value is always 1.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="34102-140">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34102-140">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="34102-141">\_Valore del tipo BIOmetrico WINBIO \_ che specifica il tipo di dati biometrici a cui si fa riferimento nel record di informazioni biometriche.</span><span class="sxs-lookup"><span data-stu-id="34102-141">A WINBIO\_BIOMETRIC\_TYPE value that specifies the type of biometric data referenced in the biometric information record.</span></span> <span data-ttu-id="34102-142">Attualmente è supportata solo l' **\_ \_ impronta digitale di tipo WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="34102-142">Currently only **WINBIO\_TYPE\_FINGERPRINT** is supported.</span></span> <span data-ttu-id="34102-143">Per altre informazioni, vedere [**\_ costanti WINBIO di \_ tipo biometrico**](winbio-biometric-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="34102-143">For more information, see [**WINBIO\_BIOMETRIC\_TYPE Constants**](winbio-biometric-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="34102-144">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="34102-144">**Subtype**</span></span>
</dt> <dd>

<span data-ttu-id="34102-145">Valore **del \_ \_ SOTTOtipo biometrico WINBIO** che specifica il Sottofattore associato ai dati biometrici.</span><span class="sxs-lookup"><span data-stu-id="34102-145">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="34102-146">Per altre informazioni, vedere osservazioni e [**\_ \_ costanti SOTTOtipi biometrici WINBIO**](winbio-biometric-subtype-constants.md).</span><span class="sxs-lookup"><span data-stu-id="34102-146">For more information, see Remarks and [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="34102-147">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="34102-147">**Purpose**</span></span>
</dt> <dd>

<span data-ttu-id="34102-148">Maschera **WINBIO \_ Bir \_ purpose** che specifica l'uso previsto dei dati.</span><span class="sxs-lookup"><span data-stu-id="34102-148">A **WINBIO\_BIR\_PURPOSE** mask that specifies the intended use of the data.</span></span> <span data-ttu-id="34102-149">Può trattarsi di un **or** bit per bit dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="34102-149">This can be a bitwise **OR** of the following values.</span></span> <span data-ttu-id="34102-150">Per altre informazioni, vedere [**\_ costanti per \_ lo scopo di WINBIO bir**](winbio-bir-purpose-constants.md).</span><span class="sxs-lookup"><span data-stu-id="34102-150">For more information, see [**WINBIO\_BIR\_PURPOSE Constants**](winbio-bir-purpose-constants.md).</span></span>

-   <span data-ttu-id="34102-151">\_Verifica finalità \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="34102-151">WINBIO\_PURPOSE\_VERIFY</span></span>
-   <span data-ttu-id="34102-152">\_Identificazione scopo \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="34102-152">WINBIO\_PURPOSE\_IDENTIFY</span></span>
-   <span data-ttu-id="34102-153">\_registrazione scopo \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="34102-153">WINBIO\_PURPOSE\_ENROLL</span></span>
-   <span data-ttu-id="34102-154">\_registrazione scopo \_ WINBIO \_ per la \_ Verifica</span><span class="sxs-lookup"><span data-stu-id="34102-154">WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION</span></span>
-   <span data-ttu-id="34102-155">\_registrazione scopo \_ WINBIO \_ per l' \_ Identificazione</span><span class="sxs-lookup"><span data-stu-id="34102-155">WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION</span></span>
-   <span data-ttu-id="34102-156">\_controllo scopo \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="34102-156">WINBIO\_PURPOSE\_AUDIT</span></span>

</dd> <dt>

<span data-ttu-id="34102-157">**Dataquality**</span><span class="sxs-lookup"><span data-stu-id="34102-157">**DataQuality**</span></span>
</dt> <dd>

<span data-ttu-id="34102-158">Valore che specifica la qualità relativa dei dati biometrici nel record di informazioni biometriche (BIR).</span><span class="sxs-lookup"><span data-stu-id="34102-158">A value that specifies the relative quality of the biometric data in the biometric information record (BIR).</span></span> <span data-ttu-id="34102-159">Può essere un numero intero compreso tra 0 e 100 o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="34102-159">This can be an integer from 0 to 100 or one of the following values.</span></span> <span data-ttu-id="34102-160">Per ulteriori informazioni, vedere [**WINBIO \_ Bir \_ Quality costanti**](winbio-bir-quality-constants.md).</span><span class="sxs-lookup"><span data-stu-id="34102-160">For more information, see [**WINBIO\_BIR\_QUALITY Constants**](winbio-bir-quality-constants.md).</span></span>



| <span data-ttu-id="34102-161">Valore</span><span class="sxs-lookup"><span data-stu-id="34102-161">Value</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="34102-162">Significato</span><span class="sxs-lookup"><span data-stu-id="34102-162">Meaning</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="34102-163"><dt>**WINBIO \_ DATA \_ Quality \_ Not \_ set**</dt> <dt>(( \_ qualità WINBIO bir \_ )-1)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-163"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt>((WINBIO\_BIR\_QUALITY)-1)</dt></span></span> </dl>                   | <span data-ttu-id="34102-164">Le misurazioni di qualità sono supportate dal creatore di BIR, ma in BIR non è impostato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="34102-164">Quality measurements are supported by the BIR creator but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="34102-165"><dt>**WINBIO \_ Qualità dei dati \_ \_ non \_ supportata**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-165"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt>((WINBIO\_BIR\_QUALITY)-2)</dt></span></span> </dl> | <span data-ttu-id="34102-166">Le misurazioni di qualità non sono supportate da BIR Creator.</span><span class="sxs-lookup"><span data-stu-id="34102-166">Quality measurements are not supported by the BIR creator.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="34102-167">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="34102-167">**CreationDate**</span></span>
</dt> <dd>

<span data-ttu-id="34102-168">Data e ora, in formato UTC (ora di Greenwich), in cui è stato creato il BIR.</span><span class="sxs-lookup"><span data-stu-id="34102-168">The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.</span></span>

</dd> <dt>

<span data-ttu-id="34102-169">**ValidityPeriod**</span><span class="sxs-lookup"><span data-stu-id="34102-169">**ValidityPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="34102-170">Periodo per il quale BIR è valido.</span><span class="sxs-lookup"><span data-stu-id="34102-170">The period for which the BIR is valid.</span></span>

<dl> <dt>

<span data-ttu-id="34102-171">**BeginDate**</span><span class="sxs-lookup"><span data-stu-id="34102-171">**BeginDate**</span></span>
</dt> <dd>

<span data-ttu-id="34102-172">Data e ora dell'inizio del periodo di validità dell'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="34102-172">The date and time, in Coordinated Universal Time, that the validity period starts.</span></span>

</dd> <dt>

<span data-ttu-id="34102-173">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="34102-173">**EndDate**</span></span>
</dt> <dd>

<span data-ttu-id="34102-174">Data e ora, in formato UTC (Coordinated Universal Time), in cui BIR cessa di essere valido.</span><span class="sxs-lookup"><span data-stu-id="34102-174">The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="34102-175">**BiometricDataFormat**</span><span class="sxs-lookup"><span data-stu-id="34102-175">**BiometricDataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="34102-176">Struttura [**di \_ \_ formato registrata WINBIO**](winbio-registered-format.md) che specifica il formato dati del blocco di dati standard nella struttura [**WINBIO \_ Bir**](winbio-bir.md) .</span><span class="sxs-lookup"><span data-stu-id="34102-176">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the data format of the standard data block in the [**WINBIO\_BIR**](winbio-bir.md) structure.</span></span> <span data-ttu-id="34102-177">I membri del **\_ \_ formato registrato WINBIO** non possono essere zero.</span><span class="sxs-lookup"><span data-stu-id="34102-177">The **WINBIO\_REGISTERED\_FORMAT** members cannot be zero.</span></span> <span data-ttu-id="34102-178">Per semplificare il controllo degli errori, è possibile utilizzare le costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="34102-178">You can use the following constants to simplify error checking.</span></span>



| <span data-ttu-id="34102-179">Valore</span><span class="sxs-lookup"><span data-stu-id="34102-179">Value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="34102-180">Significato</span><span class="sxs-lookup"><span data-stu-id="34102-180">Meaning</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <span data-ttu-id="34102-181"><dt>**WINBIO \_ Nessun \_ proprietario di formato \_ \_ disponibile**</dt> <dt>((ushort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-181"><dt>**WINBIO\_NO\_FORMAT\_OWNER\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl> | <span data-ttu-id="34102-182">Non è stato specificato alcun valore proprietario assegnato a IBROLI (International Biometric Industry Association).</span><span class="sxs-lookup"><span data-stu-id="34102-182">No IBIA (International Biometric Industry Association) assigned owner value has been specified.</span></span><br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <span data-ttu-id="34102-183"><dt>**WINBIO \_ Nessun \_ tipo di formato \_ \_ disponibile**</dt> <dt>((ushort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-183"><dt>**WINBIO\_NO\_FORMAT\_TYPE\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl>    | <span data-ttu-id="34102-184">Non è stato specificato alcun tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="34102-184">No format type has been specified.</span></span><br/>                                                              |



 

</dd> <dt>

<span data-ttu-id="34102-185">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="34102-185">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="34102-186">Struttura [**di \_ \_ formato registrata WINBIO**](winbio-registered-format.md) che specifica l'ID prodotto del componente che ha generato il blocco di dati standard in Bir.</span><span class="sxs-lookup"><span data-stu-id="34102-186">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the product ID of the component that generated the standard data block in the BIR.</span></span> <span data-ttu-id="34102-187">I membri del **\_ \_ formato registrato WINBIO** possono essere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="34102-187">The **WINBIO\_REGISTERED\_FORMAT** members can be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34102-188">Commenti</span><span class="sxs-lookup"><span data-stu-id="34102-188">Remarks</span></span>

<span data-ttu-id="34102-189">Il parametro *SubType* specifica il Sottofattore associato ai dati biometrici.</span><span class="sxs-lookup"><span data-stu-id="34102-189">The *Subtype* parameter specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="34102-190">Attualmente, il Windows Biometric Framework (WBF) supporta solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sui sottotipi:</span><span class="sxs-lookup"><span data-stu-id="34102-190">Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:</span></span>

-   <span data-ttu-id="34102-191">WINBIO \_ ANSI \_ 381 \_ POS \_ sconosciuta</span><span class="sxs-lookup"><span data-stu-id="34102-191">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="34102-192">WINBIO \_ ANSI \_ 381 \_ POS \_ \_ pollice RH</span><span class="sxs-lookup"><span data-stu-id="34102-192">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="34102-193">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ - \_ dito indice</span><span class="sxs-lookup"><span data-stu-id="34102-193">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="34102-194">WINBIO \_ ANSI \_ 381 \_ POS \_ \_ secondo \_ dito medio</span><span class="sxs-lookup"><span data-stu-id="34102-194">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="34102-195">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_ anulare</span><span class="sxs-lookup"><span data-stu-id="34102-195">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="34102-196">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ piccolo \_ dito</span><span class="sxs-lookup"><span data-stu-id="34102-196">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="34102-197">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="34102-197">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="34102-198">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito indice LH \_</span><span class="sxs-lookup"><span data-stu-id="34102-198">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="34102-199">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito medio SX \_</span><span class="sxs-lookup"><span data-stu-id="34102-199">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="34102-200">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ \_ dito sinistro</span><span class="sxs-lookup"><span data-stu-id="34102-200">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="34102-201">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="34102-201">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="34102-202">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ quattro \_ dita</span><span class="sxs-lookup"><span data-stu-id="34102-202">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="34102-203">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ quattro \_ dita</span><span class="sxs-lookup"><span data-stu-id="34102-203">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="34102-204">WINBIO \_ ANSI \_ 381 \_ POS \_ due \_ pollici</span><span class="sxs-lookup"><span data-stu-id="34102-204">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="34102-205">Non tentare di convalidare il valore specificato per il valore del parametro del *sottotipo* .</span><span class="sxs-lookup"><span data-stu-id="34102-205">Do not attempt to validate the value supplied for the *Subtype* parameter value.</span></span> <span data-ttu-id="34102-206">Il servizio biometria di Windows convaliderà il valore fornito prima di passarlo all'implementazione.</span><span class="sxs-lookup"><span data-stu-id="34102-206">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="34102-207">Se il valore è **WINBIO, non vi sono \_ \_ \_ informazioni** o **\_ sottotipi \_ di WINBIO**, quindi eseguire la convalida laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="34102-207">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

<span data-ttu-id="34102-208">Se viene dichiarato uno dei bit seguenti, la struttura dell' **\_ \_ intestazione WINBIO bir** non è formattata correttamente.</span><span class="sxs-lookup"><span data-stu-id="34102-208">If any of the following bits are asserted, the **WINBIO\_BIR\_HEADER** structure is not correctly formed.</span></span>


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a><span data-ttu-id="34102-209">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34102-209">Requirements</span></span>



| <span data-ttu-id="34102-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="34102-210">Requirement</span></span> | <span data-ttu-id="34102-211">Valore</span><span class="sxs-lookup"><span data-stu-id="34102-211">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34102-212">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34102-212">Minimum supported client</span></span><br/> | <span data-ttu-id="34102-213">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="34102-213">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="34102-214">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34102-214">Minimum supported server</span></span><br/> | <span data-ttu-id="34102-215">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="34102-215">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="34102-216">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34102-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="34102-217"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34102-217"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34102-218">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34102-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34102-219">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="34102-219">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="34102-220">**\_Costanti SOTTOtipi BIOmetrici WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="34102-220">**WINBIO\_BIOMETRIC\_SUBTYPE Constants**</span></span>](winbio-biometric-subtype-constants.md)
</dt> <dt>

[<span data-ttu-id="34102-221">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="34102-221">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="34102-222">**\_ \_ Costanti flag di dati WINBIO bir \_**</span><span class="sxs-lookup"><span data-stu-id="34102-222">**WINBIO\_BIR\_DATA\_FLAGS Constants**</span></span>](winbio-bir-data-flags-constants.md)
</dt> <dt>

[<span data-ttu-id="34102-223">**\_Costanti di \_ campo WINBIO Bir**</span><span class="sxs-lookup"><span data-stu-id="34102-223">**WINBIO\_BIR\_FIELD Constants**</span></span>](winbio-bir-field-constants.md)
</dt> <dt>

[<span data-ttu-id="34102-224">**Costanti WINBIO per \_ \_ finalità Bir**</span><span class="sxs-lookup"><span data-stu-id="34102-224">**WINBIO\_BIR\_PURPOSE Constants**</span></span>](winbio-bir-purpose-constants.md)
</dt> <dt>

[<span data-ttu-id="34102-225">**\_Costanti di \_ qualità WINBIO Bir**</span><span class="sxs-lookup"><span data-stu-id="34102-225">**WINBIO\_BIR\_QUALITY Constants**</span></span>](winbio-bir-quality-constants.md)
</dt> <dt>

[<span data-ttu-id="34102-226">**Costanti della versione di WINBIO \_ Bir \_**</span><span class="sxs-lookup"><span data-stu-id="34102-226">**WINBIO\_BIR\_VERSION Constants**</span></span>](winbio-bir-version-constants.md)
</dt> </dl>

 

 





