---
description: 'Image_V1_Load classe: questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106499"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="eec9b-104">Classe Load \_ dell'immagine V1 \_</span><span class="sxs-lookup"><span data-stu-id="eec9b-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="eec9b-105">Questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini.</span><span class="sxs-lookup"><span data-stu-id="eec9b-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="eec9b-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="eec9b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec9b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eec9b-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="eec9b-108">Members</span><span class="sxs-lookup"><span data-stu-id="eec9b-108">Members</span></span>

<span data-ttu-id="eec9b-109">La **classe Image \_ V1 \_ Load** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eec9b-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="eec9b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eec9b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eec9b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eec9b-111">Properties</span></span>

<span data-ttu-id="eec9b-112">La **classe Image \_ V1 \_ Load** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eec9b-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eec9b-113">FileName</span><span class="sxs-lookup"><span data-stu-id="eec9b-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec9b-114">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="eec9b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eec9b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-116">Qualificatori: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="eec9b-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="eec9b-117">Nome file ed estensione della DLL o dell'immagine eseguibile da caricare.</span><span class="sxs-lookup"><span data-stu-id="eec9b-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="eec9b-118">ImageBase</span><span class="sxs-lookup"><span data-stu-id="eec9b-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec9b-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="eec9b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eec9b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-121">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="eec9b-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="eec9b-122">Indirizzo di base dell'applicazione in cui viene caricata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="eec9b-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="eec9b-123">Imagesize</span><span class="sxs-lookup"><span data-stu-id="eec9b-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec9b-124">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="eec9b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eec9b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-126">Qualificatori: WmiDataId(2), Puntatore</span><span class="sxs-lookup"><span data-stu-id="eec9b-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="eec9b-127">Dimensioni dell'immagine caricata.</span><span class="sxs-lookup"><span data-stu-id="eec9b-127">Size of the image being loaded.</span></span>

<span data-ttu-id="eec9b-128">Quando si utilizza questa proprietà, il tipo di dati per questa proprietà è effettivamente size \_ t.</span><span class="sxs-lookup"><span data-stu-id="eec9b-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="eec9b-129">Il qualificatore puntatore viene usato per determinare se la dimensione \_ t è di 4 o 8 byte.</span><span class="sxs-lookup"><span data-stu-id="eec9b-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eec9b-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="eec9b-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eec9b-131">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="eec9b-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eec9b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eec9b-133">Qualificatori: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="eec9b-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="eec9b-134">Identifica il processo in cui viene caricata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="eec9b-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eec9b-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eec9b-135">Requirements</span></span>



| <span data-ttu-id="eec9b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec9b-136">Requirement</span></span> | <span data-ttu-id="eec9b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="eec9b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eec9b-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eec9b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="eec9b-139">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="eec9b-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="eec9b-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eec9b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="eec9b-141">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eec9b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eec9b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eec9b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec9b-143">**Immagine \_ V1**</span><span class="sxs-lookup"><span data-stu-id="eec9b-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




