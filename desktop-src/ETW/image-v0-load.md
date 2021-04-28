---
description: 'Image_V0_Load: questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106515"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="66cdf-104">Classe Image \_ V0 \_ Load</span><span class="sxs-lookup"><span data-stu-id="66cdf-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="66cdf-105">Questa classe è la classe del tipo di evento per gli eventi di caricamento delle immagini.</span><span class="sxs-lookup"><span data-stu-id="66cdf-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="66cdf-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="66cdf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="66cdf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66cdf-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="66cdf-108">Members</span><span class="sxs-lookup"><span data-stu-id="66cdf-108">Members</span></span>

<span data-ttu-id="66cdf-109">La **classe Image \_ V0 \_ Load** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="66cdf-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="66cdf-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66cdf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66cdf-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66cdf-111">Properties</span></span>

<span data-ttu-id="66cdf-112">La **classe Image \_ V0 \_ Load** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="66cdf-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66cdf-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="66cdf-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66cdf-114">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="66cdf-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66cdf-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66cdf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66cdf-116">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="66cdf-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="66cdf-117">Indirizzo di base dell'applicazione in cui viene caricata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="66cdf-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="66cdf-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="66cdf-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66cdf-119">Tipo di dati: **string**</span><span class="sxs-lookup"><span data-stu-id="66cdf-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66cdf-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66cdf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66cdf-121">Qualificatori: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="66cdf-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="66cdf-122">Nome file ed estensione della DLL o dell'immagine eseguibile da caricare.</span><span class="sxs-lookup"><span data-stu-id="66cdf-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="66cdf-123">ModuleSize</span><span class="sxs-lookup"><span data-stu-id="66cdf-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66cdf-124">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="66cdf-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66cdf-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66cdf-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66cdf-126">Qualificatori: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="66cdf-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="66cdf-127">Dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="66cdf-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66cdf-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66cdf-128">Requirements</span></span>



| <span data-ttu-id="66cdf-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="66cdf-129">Requirement</span></span> | <span data-ttu-id="66cdf-130">Valore</span><span class="sxs-lookup"><span data-stu-id="66cdf-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="66cdf-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66cdf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="66cdf-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66cdf-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="66cdf-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66cdf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="66cdf-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66cdf-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="66cdf-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66cdf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66cdf-136">**Immagine \_ V0**</span><span class="sxs-lookup"><span data-stu-id="66cdf-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




