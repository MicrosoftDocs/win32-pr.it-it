---
description: Questa classe è la classe del tipo di evento per gli eventi di caricamento di immagini. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Classe Image_V0_Load
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
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977122"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="3f5a9-104">Image \_ V0 \_ Load-classe</span><span class="sxs-lookup"><span data-stu-id="3f5a9-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="3f5a9-105">Questa classe è la classe del tipo di evento per gli eventi di caricamento di immagini.</span><span class="sxs-lookup"><span data-stu-id="3f5a9-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="3f5a9-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3f5a9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f5a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f5a9-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="3f5a9-108">Members</span><span class="sxs-lookup"><span data-stu-id="3f5a9-108">Members</span></span>

<span data-ttu-id="3f5a9-109">La classe di **\_ \_ caricamento image V0** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3f5a9-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="3f5a9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3f5a9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f5a9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3f5a9-111">Properties</span></span>

<span data-ttu-id="3f5a9-112">La classe di **\_ \_ caricamento image V0** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3f5a9-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f5a9-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="3f5a9-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f5a9-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f5a9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f5a9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f5a9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f5a9-116">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="3f5a9-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3f5a9-117">Indirizzo di base dell'applicazione in cui viene caricata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="3f5a9-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="3f5a9-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="3f5a9-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f5a9-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f5a9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f5a9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f5a9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f5a9-121">Qualificatori: WmiDataId (3), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="3f5a9-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="3f5a9-122">Nome file ed estensione della DLL o dell'immagine eseguibile da caricare.</span><span class="sxs-lookup"><span data-stu-id="3f5a9-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="3f5a9-123">ModuleSize</span><span class="sxs-lookup"><span data-stu-id="3f5a9-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f5a9-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f5a9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f5a9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f5a9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f5a9-126">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="3f5a9-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="3f5a9-127">Dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="3f5a9-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f5a9-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f5a9-128">Requirements</span></span>



| <span data-ttu-id="3f5a9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f5a9-129">Requirement</span></span> | <span data-ttu-id="3f5a9-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3f5a9-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3f5a9-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f5a9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3f5a9-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3f5a9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3f5a9-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f5a9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3f5a9-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3f5a9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3f5a9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f5a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f5a9-136">**Immagine \_ V0**</span><span class="sxs-lookup"><span data-stu-id="3f5a9-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




