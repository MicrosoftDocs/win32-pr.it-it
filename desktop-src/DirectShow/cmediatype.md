---
description: La classe CMediaType gestisce i tipi di supporto. Questa classe eredita la \_ struttura del tipo di supporto am \_ . È possibile eseguire il cast a una variabile di tipo AM \_ media \_ Type.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Classe CMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327450"
---
# <a name="cmediatype-class"></a><span data-ttu-id="63a45-105">Classe CMediaType</span><span class="sxs-lookup"><span data-stu-id="63a45-105">CMediaType class</span></span>

![gerarchia di classi CMediaType](images/mtype01.png)

<span data-ttu-id="63a45-107">La `CMediaType` classe gestisce i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="63a45-107">The `CMediaType` class manages media types.</span></span> <span data-ttu-id="63a45-108">Questa classe eredita la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="63a45-108">This class inherits the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="63a45-109">È possibile eseguire il cast a una variabile di tipo **am \_ media \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="63a45-109">It can be cast to a variable of type **AM\_MEDIA\_TYPE**.</span></span>



| <span data-ttu-id="63a45-110">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="63a45-110">Public Methods</span></span>                                                      | <span data-ttu-id="63a45-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63a45-111">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="63a45-112">**CMediaType**</span><span class="sxs-lookup"><span data-stu-id="63a45-112">**CMediaType**</span></span>](cmediatype-cmediatype.md)                         | <span data-ttu-id="63a45-113">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="63a45-113">Constructor method.</span></span>                                                            |
| [<span data-ttu-id="63a45-114">**~ CMediaType**</span><span class="sxs-lookup"><span data-stu-id="63a45-114">**~CMediaType**</span></span>](cmediatype--cmediatype.md)                       | <span data-ttu-id="63a45-115">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="63a45-115">Destructor method.</span></span>                                                             |
| [<span data-ttu-id="63a45-116">**Set**</span><span class="sxs-lookup"><span data-stu-id="63a45-116">**Set**</span></span>](cmediatype-set.md)                                       | <span data-ttu-id="63a45-117">Imposta il tipo di supporto da un altro tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="63a45-117">Sets the media type from another media type.</span></span>                                   |
| [<span data-ttu-id="63a45-118">**isValid**</span><span class="sxs-lookup"><span data-stu-id="63a45-118">**IsValid**</span></span>](cmediatype-isvalid.md)                               | <span data-ttu-id="63a45-119">Determina se un tipo principale è stato assegnato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="63a45-119">Determines whether a major type has been assigned to this object.</span></span>              |
| [<span data-ttu-id="63a45-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="63a45-120">**Type**</span></span>](cmediatype-type.md)                                     | <span data-ttu-id="63a45-121">Recupera il tipo principale.</span><span class="sxs-lookup"><span data-stu-id="63a45-121">Retrieves the major type.</span></span>                                                      |
| [<span data-ttu-id="63a45-122">**SetType**</span><span class="sxs-lookup"><span data-stu-id="63a45-122">**SetType**</span></span>](cmediatype-settype.md)                               | <span data-ttu-id="63a45-123">Specifica il tipo principale.</span><span class="sxs-lookup"><span data-stu-id="63a45-123">Specifies the major type.</span></span>                                                      |
| [<span data-ttu-id="63a45-124">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="63a45-124">**Subtype**</span></span>](cmediatype-subtype.md)                               | <span data-ttu-id="63a45-125">Recupera il sottotipo.</span><span class="sxs-lookup"><span data-stu-id="63a45-125">Retrieves the subtype.</span></span>                                                         |
| [<span data-ttu-id="63a45-126">**SetSubtype**</span><span class="sxs-lookup"><span data-stu-id="63a45-126">**SetSubtype**</span></span>](cmediatype-setsubtype.md)                         | <span data-ttu-id="63a45-127">Specifica il sottotipo.</span><span class="sxs-lookup"><span data-stu-id="63a45-127">Specifies the subtype.</span></span>                                                         |
| [<span data-ttu-id="63a45-128">**IsFixedSize**</span><span class="sxs-lookup"><span data-stu-id="63a45-128">**IsFixedSize**</span></span>](cmediatype-isfixedsize.md)                       | <span data-ttu-id="63a45-129">Determina se gli esempi hanno dimensioni fisse o variabili.</span><span class="sxs-lookup"><span data-stu-id="63a45-129">Determines if the samples have a fixed size or a variable size.</span></span>                |
| [<span data-ttu-id="63a45-130">**IsTemporalCompressed**</span><span class="sxs-lookup"><span data-stu-id="63a45-130">**IsTemporalCompressed**</span></span>](cmediatype-istemporalcompressed.md)     | <span data-ttu-id="63a45-131">Determina se il flusso usa la compressione temporale.</span><span class="sxs-lookup"><span data-stu-id="63a45-131">Determines if the stream uses temporal compression.</span></span>                            |
| [<span data-ttu-id="63a45-132">**GetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="63a45-132">**GetSampleSize**</span></span>](cmediatype-getsamplesize.md)                   | <span data-ttu-id="63a45-133">Recupera le dimensioni del campione.</span><span class="sxs-lookup"><span data-stu-id="63a45-133">Retrieves the sample size.</span></span>                                                     |
| [<span data-ttu-id="63a45-134">**SetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="63a45-134">**SetSampleSize**</span></span>](cmediatype-setsamplesize.md)                   | <span data-ttu-id="63a45-135">Specifica una dimensione del campione fissa o specifica che gli esempi hanno una dimensione variabile.</span><span class="sxs-lookup"><span data-stu-id="63a45-135">Specifies a fixed sample size, or specifies that samples have a variable size.</span></span> |
| [<span data-ttu-id="63a45-136">**SetVariableSize**</span><span class="sxs-lookup"><span data-stu-id="63a45-136">**SetVariableSize**</span></span>](cmediatype-setvariablesize.md)               | <span data-ttu-id="63a45-137">Specifica che gli esempi non hanno dimensioni fisse.</span><span class="sxs-lookup"><span data-stu-id="63a45-137">Specifies that samples do not have a fixed size.</span></span>                               |
| [<span data-ttu-id="63a45-138">**SetTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="63a45-138">**SetTemporalCompression**</span></span>](cmediatype-settemporalcompression.md) | <span data-ttu-id="63a45-139">Specifica se gli esempi vengono compressi con la compressione temporale.</span><span class="sxs-lookup"><span data-stu-id="63a45-139">Specifies whether samples are compressed using temporal compression.</span></span>           |
| [<span data-ttu-id="63a45-140">**Formato**</span><span class="sxs-lookup"><span data-stu-id="63a45-140">**Format**</span></span>](cmediatype-format.md)                                 | <span data-ttu-id="63a45-141">Recupera un puntatore al blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="63a45-141">Retrieves a pointer to the format block.</span></span>                                       |
| [<span data-ttu-id="63a45-142">**FormatLength**</span><span class="sxs-lookup"><span data-stu-id="63a45-142">**FormatLength**</span></span>](cmediatype-formatlength.md)                     | <span data-ttu-id="63a45-143">Recupera la lunghezza del blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="63a45-143">Retrieves the length of the format block.</span></span>                                      |
| [<span data-ttu-id="63a45-144">**SetFormatType**</span><span class="sxs-lookup"><span data-stu-id="63a45-144">**SetFormatType**</span></span>](cmediatype-setformattype.md)                   | <span data-ttu-id="63a45-145">Specifica il tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="63a45-145">Specifies the format type.</span></span>                                                     |
| [<span data-ttu-id="63a45-146">**FormatType**</span><span class="sxs-lookup"><span data-stu-id="63a45-146">**FormatType**</span></span>](cmediatype-formattype.md)                         | <span data-ttu-id="63a45-147">Recupera il tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="63a45-147">Retrieves the format type.</span></span>                                                     |
| [<span data-ttu-id="63a45-148">**SetFormat**</span><span class="sxs-lookup"><span data-stu-id="63a45-148">**SetFormat**</span></span>](cmediatype-setformat.md)                           | <span data-ttu-id="63a45-149">Specifica il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="63a45-149">Specifies the format block.</span></span>                                                    |
| [<span data-ttu-id="63a45-150">**ResetFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="63a45-150">**ResetFormatBuffer**</span></span>](cmediatype-resetformatbuffer.md)           | <span data-ttu-id="63a45-151">Elimina il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="63a45-151">Deletes the format block.</span></span>                                                      |
| [<span data-ttu-id="63a45-152">**AllocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="63a45-152">**AllocFormatBuffer**</span></span>](cmediatype-allocformatbuffer.md)           | <span data-ttu-id="63a45-153">Alloca memoria per il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="63a45-153">Allocates memory for the format block.</span></span>                                         |
| [<span data-ttu-id="63a45-154">**ReallocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="63a45-154">**ReallocFormatBuffer**</span></span>](cmediatype-reallocformatbuffer.md)       | <span data-ttu-id="63a45-155">Rialloca il blocco di formato in una nuova dimensione.</span><span class="sxs-lookup"><span data-stu-id="63a45-155">Reallocates the format block to a new size.</span></span>                                    |
| [<span data-ttu-id="63a45-156">**InitMediaType**</span><span class="sxs-lookup"><span data-stu-id="63a45-156">**InitMediaType**</span></span>](cmediatype-initmediatype.md)                   | <span data-ttu-id="63a45-157">Inizializza il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="63a45-157">Initializes the media type.</span></span>                                                    |
| [<span data-ttu-id="63a45-158">**MatchesPartial**</span><span class="sxs-lookup"><span data-stu-id="63a45-158">**MatchesPartial**</span></span>](cmediatype-matchespartial.md)                 | <span data-ttu-id="63a45-159">Determina se questo tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.</span><span class="sxs-lookup"><span data-stu-id="63a45-159">Determines if this media type matches a partially specified media type.</span></span>        |
| [<span data-ttu-id="63a45-160">**IsPartiallySpecified**</span><span class="sxs-lookup"><span data-stu-id="63a45-160">**IsPartiallySpecified**</span></span>](cmediatype-ispartiallyspecified.md)     | <span data-ttu-id="63a45-161">Determina se il tipo di supporto è parzialmente definito.</span><span class="sxs-lookup"><span data-stu-id="63a45-161">Determines if the media type is partially defined.</span></span>                             |
| <span data-ttu-id="63a45-162">Operatori</span><span class="sxs-lookup"><span data-stu-id="63a45-162">Operators</span></span>                                                           | <span data-ttu-id="63a45-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63a45-163">Description</span></span>                                                                    |
| [<span data-ttu-id="63a45-164">**operatore =**</span><span class="sxs-lookup"><span data-stu-id="63a45-164">**operator =**</span></span>](cmediatype-operator-.md)                          | <span data-ttu-id="63a45-165">Consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="63a45-165">Overloads the assignment operator to copy a media type.</span></span>                        |
| [<span data-ttu-id="63a45-166">**operatore = =**</span><span class="sxs-lookup"><span data-stu-id="63a45-166">**operator ==**</span></span>](cmediatype-operator--.md)                        | <span data-ttu-id="63a45-167">Verifica l'uguaglianza tra oggetti `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="63a45-167">Tests for equality between `CMediaType` objects.</span></span>                               |
| [<span data-ttu-id="63a45-168">**operatore! =**</span><span class="sxs-lookup"><span data-stu-id="63a45-168">**operator !=**</span></span>](cmediatype-operator-neq.md)                      | <span data-ttu-id="63a45-169">Verifica la disuguaglianza tra oggetti `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="63a45-169">Tests for inequality between `CMediaType` objects.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="63a45-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63a45-170">Requirements</span></span>



| <span data-ttu-id="63a45-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a45-171">Requirement</span></span> | <span data-ttu-id="63a45-172">Valore</span><span class="sxs-lookup"><span data-stu-id="63a45-172">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a45-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63a45-173">Header</span></span><br/>  | <dl> <span data-ttu-id="63a45-174"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63a45-174"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="63a45-175">Libreria</span><span class="sxs-lookup"><span data-stu-id="63a45-175">Library</span></span><br/> | <dl> <span data-ttu-id="63a45-176"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63a45-176"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




