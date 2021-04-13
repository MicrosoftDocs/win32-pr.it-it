---
title: Struttura WINBIO_BDB_ANSI_381_RECORD ( \_ tipi WINBIO. h)
description: Contiene informazioni su una singola impronta digitale o un esempio di Palma da un utente finale.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- Struttura di WINBIO_BDB_ANSI_381_RECORD Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400282"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a><span data-ttu-id="6589f-104">\_Struttura di record WINBIO BDB \_ ANSI \_ 381 \_</span><span class="sxs-lookup"><span data-stu-id="6589f-104">WINBIO\_BDB\_ANSI\_381\_RECORD structure</span></span>

<span data-ttu-id="6589f-105">La struttura di **\_ record WINBIO BDB \_ ANSI \_ 381 \_** contiene informazioni su una singola impronta digitale o un esempio di Palma da un utente finale.</span><span class="sxs-lookup"><span data-stu-id="6589f-105">The **WINBIO\_BDB\_ANSI\_381\_RECORD** structure contains information about a single fingerprint or palm sample from an end user.</span></span> <span data-ttu-id="6589f-106">Una raccolta di queste strutture è inclusa in ogni struttura di [**\_ intestazione WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md) .</span><span class="sxs-lookup"><span data-stu-id="6589f-106">A collection of these structures is included in each [**WINBIO\_BDB\_ANSI\_381\_HEADER**](winbio-bdb-ansi-381-header.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6589f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6589f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a><span data-ttu-id="6589f-108">Members</span><span class="sxs-lookup"><span data-stu-id="6589f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6589f-109">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="6589f-109">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-110">Contiene il numero di byte nella struttura più il numero di byte dei dati dell'immagine di esempio.</span><span class="sxs-lookup"><span data-stu-id="6589f-110">Contains the number of bytes in this structure plus the number of bytes of sample image data.</span></span>

</dd> <dt>

<span data-ttu-id="6589f-111">**HorizontalLineLength**</span><span class="sxs-lookup"><span data-stu-id="6589f-111">**HorizontalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-112">Specifica il numero di pixel in una riga orizzontale dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="6589f-112">Specifies the number of pixels in a horizontal line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="6589f-113">**VerticalLineLength**</span><span class="sxs-lookup"><span data-stu-id="6589f-113">**VerticalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-114">Specifica il numero di pixel in una riga verticale dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="6589f-114">Specifies the number of pixels in a vertical line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="6589f-115">**Position**</span><span class="sxs-lookup"><span data-stu-id="6589f-115">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-116">Valore **del \_ \_ SOTTOtipo biometrico WINBIO** che specifica il dito o la Palma utilizzata per generare l'esempio biometrico.</span><span class="sxs-lookup"><span data-stu-id="6589f-116">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the finger or palm used to generate the biometric sample.</span></span> <span data-ttu-id="6589f-117">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6589f-117">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6589f-118">**CountOfViews**</span><span class="sxs-lookup"><span data-stu-id="6589f-118">**CountOfViews**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-119">Deve essere impostato su uno (1);</span><span class="sxs-lookup"><span data-stu-id="6589f-119">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="6589f-120">**ViewNumber**</span><span class="sxs-lookup"><span data-stu-id="6589f-120">**ViewNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-121">Deve essere impostato su uno (1);</span><span class="sxs-lookup"><span data-stu-id="6589f-121">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="6589f-122">**ImageQuality**</span><span class="sxs-lookup"><span data-stu-id="6589f-122">**ImageQuality**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-123">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6589f-123">Reserved.</span></span> <span data-ttu-id="6589f-124">Deve essere 254 (0xFE).</span><span class="sxs-lookup"><span data-stu-id="6589f-124">This must be 254 (0xFE).</span></span>

</dd> <dt>

<span data-ttu-id="6589f-125">**ImpressionType**</span><span class="sxs-lookup"><span data-stu-id="6589f-125">**ImpressionType**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-126">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6589f-126">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6589f-127">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="6589f-127">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="6589f-128">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6589f-128">Reserved.</span></span> <span data-ttu-id="6589f-129">Deve essere impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="6589f-129">Must be set to zero (0).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6589f-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="6589f-130">Remarks</span></span>

<span data-ttu-id="6589f-131">Il membro *position* specifica l'area della mano o della palma usata per creare l'esempio biometrico.</span><span class="sxs-lookup"><span data-stu-id="6589f-131">The *Position* member specifies the area of the hand or palm used to make the biometric sample.</span></span> <span data-ttu-id="6589f-132">Il Windows Biometric Framework (WBF) supporta attualmente solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="6589f-132">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.</span></span>

-   <span data-ttu-id="6589f-133">WINBIO \_ ANSI \_ 381 \_ POS \_ sconosciuta</span><span class="sxs-lookup"><span data-stu-id="6589f-133">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="6589f-134">WINBIO \_ ANSI \_ 381 \_ POS \_ \_ pollice RH</span><span class="sxs-lookup"><span data-stu-id="6589f-134">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="6589f-135">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ - \_ dito indice</span><span class="sxs-lookup"><span data-stu-id="6589f-135">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="6589f-136">WINBIO \_ ANSI \_ 381 \_ POS \_ \_ secondo \_ dito medio</span><span class="sxs-lookup"><span data-stu-id="6589f-136">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="6589f-137">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_ anulare</span><span class="sxs-lookup"><span data-stu-id="6589f-137">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="6589f-138">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ piccolo \_ dito</span><span class="sxs-lookup"><span data-stu-id="6589f-138">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="6589f-139">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="6589f-139">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="6589f-140">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito indice LH \_</span><span class="sxs-lookup"><span data-stu-id="6589f-140">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="6589f-141">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito medio SX \_</span><span class="sxs-lookup"><span data-stu-id="6589f-141">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="6589f-142">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ \_ dito sinistro</span><span class="sxs-lookup"><span data-stu-id="6589f-142">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="6589f-143">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="6589f-143">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="6589f-144">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ quattro \_ dita</span><span class="sxs-lookup"><span data-stu-id="6589f-144">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="6589f-145">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ quattro \_ dita</span><span class="sxs-lookup"><span data-stu-id="6589f-145">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="6589f-146">WINBIO \_ ANSI \_ 381 \_ POS \_ due \_ pollici</span><span class="sxs-lookup"><span data-stu-id="6589f-146">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6589f-147">Non tentare di convalidare il valore specificato per il valore di *posizione* .</span><span class="sxs-lookup"><span data-stu-id="6589f-147">Do not attempt to validate the value supplied for the *Position* value.</span></span> <span data-ttu-id="6589f-148">Il servizio biometria di Windows convaliderà il valore fornito prima di passarlo all'implementazione.</span><span class="sxs-lookup"><span data-stu-id="6589f-148">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="6589f-149">Se il valore è **WINBIO, non vi sono \_ \_ \_ informazioni** o **\_ sottotipi \_ di WINBIO**, quindi eseguire la convalida laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="6589f-149">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6589f-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6589f-150">Requirements</span></span>



| <span data-ttu-id="6589f-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6589f-151">Requirement</span></span> | <span data-ttu-id="6589f-152">Valore</span><span class="sxs-lookup"><span data-stu-id="6589f-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6589f-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6589f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6589f-154">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6589f-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6589f-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6589f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6589f-156">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6589f-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6589f-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6589f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="6589f-158"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6589f-158"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6589f-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6589f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6589f-160">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="6589f-160">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





