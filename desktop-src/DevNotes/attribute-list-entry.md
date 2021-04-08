---
description: Rappresenta una voce nell'elenco di attributi.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Struttura ATTRIBUTE_LIST_ENTRY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877245"
---
# <a name="attribute_list_entry-structure"></a><span data-ttu-id="f1703-103">\_ \_ Struttura voce elenco attributi</span><span class="sxs-lookup"><span data-stu-id="f1703-103">ATTRIBUTE\_LIST\_ENTRY structure</span></span>

<span data-ttu-id="f1703-104">\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]</span><span class="sxs-lookup"><span data-stu-id="f1703-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="f1703-105">Rappresenta una voce nell'elenco di attributi.</span><span class="sxs-lookup"><span data-stu-id="f1703-105">Represents an entry in the attribute list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1703-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1703-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a><span data-ttu-id="f1703-107">Members</span><span class="sxs-lookup"><span data-stu-id="f1703-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1703-108">**AttributeTypeCode**</span><span class="sxs-lookup"><span data-stu-id="f1703-108">**AttributeTypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-109">Codice del tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="f1703-109">The attribute type code.</span></span>



| <span data-ttu-id="f1703-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f1703-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="f1703-111">Significato</span><span class="sxs-lookup"><span data-stu-id="f1703-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="f1703-112"><dt>**$Standard \_**</dt> <dt>0x10</dt> informazioni</span><span class="sxs-lookup"><span data-stu-id="f1703-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="f1703-113">Attributi di file (ad esempio di sola lettura e di archivio), timestamp (ad esempio, creazione di file e Ultima modifica) e conteggio dei collegamenti reali.</span><span class="sxs-lookup"><span data-stu-id="f1703-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="f1703-114"><dt>**$Attribute \_ ELENCAre**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="f1703-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="f1703-115">Elenco di attributi che compongono il file e il riferimento al file del record del file MFT in cui si trova ogni attributo.</span><span class="sxs-lookup"><span data-stu-id="f1703-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="f1703-116"><dt>**$File \_ NOME**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="f1703-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="f1703-117">Nome del file, in caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="f1703-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="f1703-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="f1703-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="f1703-119">Identificatore di oggetto a 16 byte assegnato dal servizio di rilevamento dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="f1703-119">An 16-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="f1703-120"><dt>**$Volume \_ NOME**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="f1703-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="f1703-121">Etichetta del volume.</span><span class="sxs-lookup"><span data-stu-id="f1703-121">The volume label.</span></span> <span data-ttu-id="f1703-122">Presente nel file di $Volume.</span><span class="sxs-lookup"><span data-stu-id="f1703-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="f1703-123"><dt>**$Volume \_**</dt> <dt>0x70</dt> informazioni</span><span class="sxs-lookup"><span data-stu-id="f1703-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="f1703-124">Informazioni sul volume.</span><span class="sxs-lookup"><span data-stu-id="f1703-124">The volume information.</span></span> <span data-ttu-id="f1703-125">Presente nel file di $Volume.</span><span class="sxs-lookup"><span data-stu-id="f1703-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="f1703-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="f1703-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="f1703-127">Contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="f1703-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="f1703-128"><dt>**$Index \_**</dt> <dt>0x90</dt> radice</span><span class="sxs-lookup"><span data-stu-id="f1703-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="f1703-129">Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f1703-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="f1703-130"><dt>**$Index \_**</dt> <dt>Messaggi 0XA0</dt> di allocazione</span><span class="sxs-lookup"><span data-stu-id="f1703-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="f1703-131">Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f1703-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="f1703-132"><dt>**$Bitmap**</dt> <dt>0XB0</dt></span><span class="sxs-lookup"><span data-stu-id="f1703-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="f1703-133">Indice bitmap per una directory di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f1703-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="f1703-134"><dt>**$REPARSE \_ PUNTO**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="f1703-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="f1703-135">Dati di reparse point.</span><span class="sxs-lookup"><span data-stu-id="f1703-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="f1703-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="f1703-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-137">Dimensioni della struttura, più il buffer dei nomi facoltativo, in byte.</span><span class="sxs-lookup"><span data-stu-id="f1703-137">The size of this structure, plus the optional name buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f1703-138">**AttributeNameLength**</span><span class="sxs-lookup"><span data-stu-id="f1703-138">**AttributeNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-139">Dimensioni del nome di attributo facoltativo, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="f1703-139">The size of the optional attribute name, in characters.</span></span> <span data-ttu-id="f1703-140">Se esiste un nome, questo valore è diverso da zero e la struttura viene seguita immediatamente da una stringa Unicode del numero di caratteri specificato.</span><span class="sxs-lookup"><span data-stu-id="f1703-140">If a name exists, this value is nonzero and the structure is followed immediately by a Unicode string of the specified number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="f1703-141">**AttributeNameOffset**</span><span class="sxs-lookup"><span data-stu-id="f1703-141">**AttributeNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-142">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f1703-142">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f1703-143">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="f1703-143">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-144">Il numero di cluster virtuale più basso (VCN) per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="f1703-144">The lowest virtual cluster number (VCN) for this attribute.</span></span> <span data-ttu-id="f1703-145">Questo membro è zero a meno che l'attributo non richieda più segmenti di record di file e, a meno che questa voce non sia un riferimento a un segmento diverso da quello prima.</span><span class="sxs-lookup"><span data-stu-id="f1703-145">This member is zero unless the attribute requires multiple file record segments and unless this entry is a reference to a segment other than the first one.</span></span> <span data-ttu-id="f1703-146">In questo caso, questo valore è il VCN più basso descritto dal segmento a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="f1703-146">In this case, this value is the lowest VCN that is described by the referenced segment.</span></span>

</dd> <dt>

<span data-ttu-id="f1703-147">**SegmentReference**</span><span class="sxs-lookup"><span data-stu-id="f1703-147">**SegmentReference**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-148">Segmento della tabella file master (MFT) in cui risiede l'attributo.</span><span class="sxs-lookup"><span data-stu-id="f1703-148">The master file table (MFT) segment in which the attribute resides.</span></span> <span data-ttu-id="f1703-149">Vedere informazioni di [**\_ \_ riferimento sul segmento MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f1703-149">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1703-150">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f1703-150">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-151">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f1703-151">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f1703-152">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="f1703-152">**AttributeName**</span></span>
</dt> <dd>

<span data-ttu-id="f1703-153">Inizio del nome di attributo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1703-153">The start of the optional attribute name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1703-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1703-154">Remarks</span></span>

<span data-ttu-id="f1703-155">L'elenco degli attributi è un elenco ordinato di strutture di **\_ \_ voci dell'elenco di attributi** allineati a quadrupla.</span><span class="sxs-lookup"><span data-stu-id="f1703-155">The attributes list is an ordered list of quadword-aligned **ATTRIBUTE\_LIST\_ENTRY** structures.</span></span> <span data-ttu-id="f1703-156">Questo elenco viene ordinato prima in base al codice del tipo di attributo e quindi in base al nome dell'attributo (se presente).</span><span class="sxs-lookup"><span data-stu-id="f1703-156">This list is ordered first by the attribute type code and then by the attribute name (if present).</span></span> <span data-ttu-id="f1703-157">Due attributi non possono avere lo stesso codice di tipo, nome e VCN più basso.</span><span class="sxs-lookup"><span data-stu-id="f1703-157">No two attributes can have the same type code, name, and lowest VCN.</span></span> <span data-ttu-id="f1703-158">Pertanto, può essere presente al massimo un attributo per ogni codice del tipo senza un nome.</span><span class="sxs-lookup"><span data-stu-id="f1703-158">Therefore, there can be at most one attribute for each type code without a name.</span></span>

<span data-ttu-id="f1703-159">Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="f1703-159">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="f1703-160">Si noti che non è presente alcun file di intestazione associato per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="f1703-160">Note that there is no associated header file for this structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1703-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1703-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1703-162">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="f1703-162">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
