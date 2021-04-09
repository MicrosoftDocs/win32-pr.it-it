---
description: Rappresenta un record di attributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Struttura ATTRIBUTE_RECORD_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877242"
---
# <a name="attribute_record_header-structure"></a><span data-ttu-id="e177f-103">Struttura dell'intestazione del \_ record degli attributi \_</span><span class="sxs-lookup"><span data-stu-id="e177f-103">ATTRIBUTE\_RECORD\_HEADER structure</span></span>

<span data-ttu-id="e177f-104">\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]</span><span class="sxs-lookup"><span data-stu-id="e177f-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="e177f-105">Rappresenta un record di attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-105">Represents an attribute record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e177f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e177f-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="e177f-107">Members</span><span class="sxs-lookup"><span data-stu-id="e177f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e177f-108">**TypeCode**</span><span class="sxs-lookup"><span data-stu-id="e177f-108">**TypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-109">Codice del tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-109">The attribute type code.</span></span>



| <span data-ttu-id="e177f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e177f-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="e177f-111">Significato</span><span class="sxs-lookup"><span data-stu-id="e177f-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="e177f-112"><dt>**$Standard \_**</dt> <dt>0x10</dt> informazioni</span><span class="sxs-lookup"><span data-stu-id="e177f-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="e177f-113">Attributi di file (ad esempio di sola lettura e di archivio), timestamp (ad esempio, creazione di file e Ultima modifica) e conteggio dei collegamenti reali.</span><span class="sxs-lookup"><span data-stu-id="e177f-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="e177f-114"><dt>**$Attribute \_ ELENCAre**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="e177f-115">Elenco di attributi che compongono il file e il riferimento al file del record del file MFT in cui si trova ogni attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="e177f-116"><dt>**$File \_ NOME**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="e177f-117">Nome del file, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="e177f-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="e177f-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="e177f-119">Identificatore di oggetto a 64 byte assegnato dal servizio di rilevamento dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="e177f-119">An 64-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="e177f-120"><dt>**$Volume \_ NOME**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="e177f-121">Etichetta del volume.</span><span class="sxs-lookup"><span data-stu-id="e177f-121">The volume label.</span></span> <span data-ttu-id="e177f-122">Presente nel file di $Volume.</span><span class="sxs-lookup"><span data-stu-id="e177f-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="e177f-123"><dt>**$Volume \_**</dt> <dt>0x70</dt> informazioni</span><span class="sxs-lookup"><span data-stu-id="e177f-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="e177f-124">Informazioni sul volume.</span><span class="sxs-lookup"><span data-stu-id="e177f-124">The volume information.</span></span> <span data-ttu-id="e177f-125">Presente nel file di $Volume.</span><span class="sxs-lookup"><span data-stu-id="e177f-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="e177f-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="e177f-127">Contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="e177f-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="e177f-128"><dt>**$Index \_**</dt> <dt>0x90</dt> radice</span><span class="sxs-lookup"><span data-stu-id="e177f-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="e177f-129">Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e177f-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="e177f-130"><dt>**$Index \_**</dt> <dt>Messaggi 0XA0</dt> di allocazione</span><span class="sxs-lookup"><span data-stu-id="e177f-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="e177f-131">Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e177f-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="e177f-132"><dt>**$Bitmap**</dt> <dt>0XB0</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="e177f-133">Indice bitmap per una directory di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e177f-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="e177f-134"><dt>**$REPARSE \_ PUNTO**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="e177f-135">Dati di reparse point.</span><span class="sxs-lookup"><span data-stu-id="e177f-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e177f-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="e177f-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-137">Dimensioni, in byte, del record di attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-137">The size of the attribute record, in bytes.</span></span> <span data-ttu-id="e177f-138">Questo valore riflette le dimensioni necessarie per la variante del record ed è sempre arrotondato al limite quadrupla più vicino.</span><span class="sxs-lookup"><span data-stu-id="e177f-138">This value reflects the required size for the record variant and is always rounded to the nearest quadword boundary.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-139">**FormCode**</span><span class="sxs-lookup"><span data-stu-id="e177f-139">**FormCode**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-140">Codice del modulo dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-140">The attribute form code.</span></span>



| <span data-ttu-id="e177f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e177f-141">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="e177f-142">Significato</span><span class="sxs-lookup"><span data-stu-id="e177f-142">Meaning</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <span data-ttu-id="e177f-143"><dt>**Residente \_ FORM**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-143"><dt>**RESIDENT\_FORM**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="e177f-144">Il valore è contenuto nel record del file e segue immediatamente l'intestazione del record dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-144">The value is contained in the file record and immediately follows the attribute record header.</span></span><br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <span data-ttu-id="e177f-145">Non <dt>**residente \_ MODULO**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e177f-145"><dt>**NONRESIDENT\_FORM**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="e177f-146">Il valore è contenuto in altri settori del disco.</span><span class="sxs-lookup"><span data-stu-id="e177f-146">The value is contained in other sectors on the disk.</span></span><br/>                                           |



 

</dd> <dt>

<span data-ttu-id="e177f-147">**NameLength**</span><span class="sxs-lookup"><span data-stu-id="e177f-147">**NameLength**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-148">Dimensioni del nome di attributo facoltativo, in caratteri, oppure 0 se non è presente alcun nome di attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-148">The size of the optional attribute name, in characters, or 0 if there is no attribute name.</span></span> <span data-ttu-id="e177f-149">La lunghezza massima del nome dell'attributo è di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e177f-149">The maximum attribute name length is 255 characters.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-150">**NameOffset**</span><span class="sxs-lookup"><span data-stu-id="e177f-150">**NameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-151">Offset del nome dell'attributo dall'inizio del record di attributo, espresso in byte.</span><span class="sxs-lookup"><span data-stu-id="e177f-151">The offset of the attribute name from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="e177f-152">Se il membro **NameLength** è 0, questo membro non è definito.</span><span class="sxs-lookup"><span data-stu-id="e177f-152">If the **NameLength** member is 0, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-153">**Flag**</span><span class="sxs-lookup"><span data-stu-id="e177f-153">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-154">Flag di attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-154">The attribute flags.</span></span>

<dl> <dt>

<span data-ttu-id="e177f-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Attributo \_ \_ \_ Maschera di compressione dei flag** (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="e177f-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE\_FLAG\_COMPRESSION\_MASK** (0x00FF)</span></span>
</dt> <dt>

<span data-ttu-id="e177f-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Attributo \_ FLAG \_ sparse** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="e177f-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE\_FLAG\_SPARSE** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="e177f-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Attributo \_ FLAG \_ crittografato** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="e177f-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE\_FLAG\_ENCRYPTED** (0x4000)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e177f-158">**Istanza**</span><span class="sxs-lookup"><span data-stu-id="e177f-158">**Instance**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-159">Istanza univoca per questo attributo nel record di file.</span><span class="sxs-lookup"><span data-stu-id="e177f-159">The unique instance for this attribute in the file record.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-160">**Form**</span><span class="sxs-lookup"><span data-stu-id="e177f-160">**Form**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-161">Se il membro **FormCode** è \_ un form residente, l'Unione è una struttura **residente** .</span><span class="sxs-lookup"><span data-stu-id="e177f-161">If the **FormCode** member is RESIDENT\_FORM, the union is a **Resident** structure.</span></span> <span data-ttu-id="e177f-162">Se **FormCode** è \_ un modulo non residente, l'Unione è una struttura non **residente** .</span><span class="sxs-lookup"><span data-stu-id="e177f-162">If **FormCode** is NONRESIDENT\_FORM, the union is a **Nonresident** structure.</span></span>

<dl> <dt>

<span data-ttu-id="e177f-163">**Residenti**</span><span class="sxs-lookup"><span data-stu-id="e177f-163">**Resident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e177f-164">**ValueLength**</span><span class="sxs-lookup"><span data-stu-id="e177f-164">**ValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-165">Dimensioni in byte del valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-165">The size of the attribute value, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-166">**ValueOffset**</span><span class="sxs-lookup"><span data-stu-id="e177f-166">**ValueOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-167">Offset del valore dall'inizio del record di attributo, espresso in byte.</span><span class="sxs-lookup"><span data-stu-id="e177f-167">The offset to the value from the start of the attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-168">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="e177f-168">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-169">Riservato.</span><span class="sxs-lookup"><span data-stu-id="e177f-169">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e177f-170">**Non residente**</span><span class="sxs-lookup"><span data-stu-id="e177f-170">**Nonresident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e177f-171">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="e177f-171">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-172">Il numero di cluster virtuale più basso (VCN) coperto da questo record di attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-172">The lowest virtual cluster number (VCN) covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-173">**HighestVcn**</span><span class="sxs-lookup"><span data-stu-id="e177f-173">**HighestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-174">VCN più alto coperto da questo record di attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-174">The highest VCN covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-175">**MappingPairsOffset**</span><span class="sxs-lookup"><span data-stu-id="e177f-175">**MappingPairsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-176">Offset della matrice delle coppie di mapping dall'inizio del record di attributo, espresso in byte.</span><span class="sxs-lookup"><span data-stu-id="e177f-176">The offset to the mapping pairs array from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="e177f-177">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e177f-177">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-178">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="e177f-178">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-179">Riservato.</span><span class="sxs-lookup"><span data-stu-id="e177f-179">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-180">**AllocatedLength**</span><span class="sxs-lookup"><span data-stu-id="e177f-180">**AllocatedLength**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-181">Dimensione allocata del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="e177f-181">The allocated size of the file, in bytes.</span></span> <span data-ttu-id="e177f-182">Questo valore è un multiplo pari delle dimensioni del cluster.</span><span class="sxs-lookup"><span data-stu-id="e177f-182">This value is an even multiple of the cluster size.</span></span> <span data-ttu-id="e177f-183">Questo membro non è valido se il membro **LowestVcn** è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e177f-183">This member is not valid if the **LowestVcn** member is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-184">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="e177f-184">**FileSize**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-185">Dimensioni del file (byte più alto che possono essere lette più 1), in byte.</span><span class="sxs-lookup"><span data-stu-id="e177f-185">The file size (highest byte that can be read plus 1), in bytes.</span></span> <span data-ttu-id="e177f-186">Questo membro non è valido se **LowestVcn** è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e177f-186">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-187">**ValidDataLength**</span><span class="sxs-lookup"><span data-stu-id="e177f-187">**ValidDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-188">Lunghezza dei dati valida (byte più alto inizializzato più 1), in byte.</span><span class="sxs-lookup"><span data-stu-id="e177f-188">The valid data length (highest initialized byte plus 1), in bytes.</span></span> <span data-ttu-id="e177f-189">Questo valore viene arrotondato al limite del cluster più vicino.</span><span class="sxs-lookup"><span data-stu-id="e177f-189">This value is rounded to the nearest cluster boundary.</span></span> <span data-ttu-id="e177f-190">Questo membro non è valido se **LowestVcn** è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e177f-190">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="e177f-191">**TotalAllocated**</span><span class="sxs-lookup"><span data-stu-id="e177f-191">**TotalAllocated**</span></span>
</dt> <dd>

<span data-ttu-id="e177f-192">Totale allocato per il file (la somma dei cluster allocati).</span><span class="sxs-lookup"><span data-stu-id="e177f-192">The total allocated for the file (the sum of the allocated clusters).</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e177f-193">Commenti</span><span class="sxs-lookup"><span data-stu-id="e177f-193">Remarks</span></span>

<span data-ttu-id="e177f-194">Si noti che non è presente alcun file di intestazione associato per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="e177f-194">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="e177f-195">Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="e177f-195">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="e177f-196">I record di attributo sono sempre allineati su un limite di quadrupla.</span><span class="sxs-lookup"><span data-stu-id="e177f-196">Attribute records are always aligned on a quadword boundary.</span></span>

<span data-ttu-id="e177f-197">Se l'attributo non è residente, l'intestazione del record di attributo contiene un elenco di informazioni di recupero che forniscono un mapping tra VCN e il numero di cluster logico (LCN) per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="e177f-197">If the attribute is nonresident, the attribute record header contains a list of retrieval information that provides a mapping between VCN and logical cluster number (LCN) for the attribute.</span></span> <span data-ttu-id="e177f-198">Se le informazioni di recupero non rientrano nel segmento di file di base, è possibile archiviarle in un segmento di record di file esterno.</span><span class="sxs-lookup"><span data-stu-id="e177f-198">If the retrieval information does not fit in the base file segment, it can be stored in an external file record segment by itself.</span></span> <span data-ttu-id="e177f-199">Se ancora non rientra in un segmento di record di file esterno, esiste un provisioning nell'elenco di attributi per contenere più voci per un attributo che richiede informazioni aggiuntive sul recupero.</span><span class="sxs-lookup"><span data-stu-id="e177f-199">If it still does not fit into one external file record segment, there is a provision in the attribute list to contain multiple entries for an attribute that requires additional retrieval information.</span></span>

<span data-ttu-id="e177f-200">La matrice di coppie di mapping è archiviata in un formato compresso e presuppone che le informazioni vengano decompresse e memorizzate nella cache dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e177f-200">The mapping pairs array is stored in a compressed form and assumes that the information is decompressed and cached by the system.</span></span> <span data-ttu-id="e177f-201">È costituito da una serie di coppie NextVcn/CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="e177f-201">It consists of a series of NextVcn/CurrentLcn pairs.</span></span> <span data-ttu-id="e177f-202">Ad esempio, se un file ha una singola esecuzione di 8 cluster a partire da LCN 128 e il file inizia con LowestVcn 0, la matrice di coppie di mapping avrà solo una voce, ovvero NextVcn = 8 e CurrentLcn = 128.</span><span class="sxs-lookup"><span data-stu-id="e177f-202">For example, if a file has a single run of 8 clusters starting at LCN 128 and the file starts at LowestVcn 0, then the mapping pairs array has just one entry, which is NextVcn=8 and CurrentLcn=128.</span></span> <span data-ttu-id="e177f-203">La matrice è un flusso di byte che archivia le modifiche apportate alle variabili di lavoro quando elaborate in sequenza.</span><span class="sxs-lookup"><span data-stu-id="e177f-203">The array is a byte stream that stores the changes to the working variables when processed sequentially.</span></span> <span data-ttu-id="e177f-204">Il flusso di byte deve essere interpretato come un flusso con terminazione zero di tripli, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e177f-204">The byte stream is to be interpreted as a zero-terminated stream of triples, as follows:</span></span>

<span data-ttu-id="e177f-205">conteggio byte = *v* + (*l* \* 16)</span><span class="sxs-lookup"><span data-stu-id="e177f-205">count byte = *v* + (*l* \* 16)</span></span>

<span data-ttu-id="e177f-206">dove *v* è il numero di byte VCN di ordine inferiore modificati e *l* è il numero di byte LCN di ordine inferiore modificati.</span><span class="sxs-lookup"><span data-stu-id="e177f-206">where *v* is the number of changed low-order VCN bytes and *l* is the number of changed low-order LCN bytes.</span></span>

<span data-ttu-id="e177f-207">L'algoritmo di decompressione è il seguente:</span><span class="sxs-lookup"><span data-stu-id="e177f-207">The decompression algorithm is as follows:</span></span>

1.  <span data-ttu-id="e177f-208">Inizializzare NextVcn su `Attribute->LowestVcn` e CurrentLcn su 0.</span><span class="sxs-lookup"><span data-stu-id="e177f-208">Initialize NextVcn to `Attribute->LowestVcn` and CurrentLcn to 0.</span></span>
2.  <span data-ttu-id="e177f-209">Inizializza il puntatore del flusso di byte in `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .</span><span class="sxs-lookup"><span data-stu-id="e177f-209">Initialize the byte stream pointer to `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset`.</span></span>
3.  <span data-ttu-id="e177f-210">Impostare CurrentVcn su NextVcn.</span><span class="sxs-lookup"><span data-stu-id="e177f-210">Set CurrentVcn to NextVcn.</span></span>
4.  <span data-ttu-id="e177f-211">Legge il byte successivo dal flusso.</span><span class="sxs-lookup"><span data-stu-id="e177f-211">Read the next byte from the stream.</span></span> <span data-ttu-id="e177f-212">Se è 0, interrompere; altrimenti estrarre *v* e *l* come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e177f-212">If it is 0, then break; else extract *v* and *l* as previously described.</span></span>
5.  <span data-ttu-id="e177f-213">Interpretare i successivi *v* byte come una quantità con segno, con prima il byte di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="e177f-213">Interpret the next *v* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="e177f-214">Decomprimere il segno, esteso in 64 bit, e aggiungerlo a NextVcn.</span><span class="sxs-lookup"><span data-stu-id="e177f-214">Unpack it sign-extended into 64 bits and add it to NextVcn.</span></span>
6.  <span data-ttu-id="e177f-215">Interpretare i successivi *l* byte come una quantità con segno, con prima il byte di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="e177f-215">Interpret the next *l* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="e177f-216">Decomprimere il segno, esteso in 64 bit, e aggiungerlo a CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="e177f-216">Unpack it sign-extended into 64 bits and add it to CurrentLcn.</span></span> <span data-ttu-id="e177f-217">Se l'oggetto produce un valore CurrentLcn pari a 0, il valore di VCNs da CurrentVcn a NextVcn-1 non è allocato.</span><span class="sxs-lookup"><span data-stu-id="e177f-217">If this produces a CurrentLcn of 0, then the VCNs from CurrentVcn to NextVcn–1 are unallocated.</span></span>
7.  <span data-ttu-id="e177f-218">Aggiornare le informazioni di mapping memorizzate nella cache da CurrentVcn, NextVcn e CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="e177f-218">Update the cached mapping information from CurrentVcn, NextVcn, and CurrentLcn.</span></span>
8.  <span data-ttu-id="e177f-219">Andare al passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="e177f-219">Go to step 3.</span></span>

## <a name="see-also"></a><span data-ttu-id="e177f-220">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e177f-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e177f-221">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="e177f-221">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
