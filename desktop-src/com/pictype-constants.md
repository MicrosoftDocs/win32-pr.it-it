---
title: Costanti PICTYPE (OleCtl. h)
description: Descrive il tipo di un oggetto Picture come restituito da IPicture Get \_ Type, nonché per descrivere il tipo di immagine nel membro picType della struttura PICTDESC che viene passata a OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301282"
---
# <a name="pictype-constants"></a><span data-ttu-id="e63c2-103">Costanti PICTYPE</span><span class="sxs-lookup"><span data-stu-id="e63c2-103">PICTYPE Constants</span></span>

<span data-ttu-id="e63c2-104">Descrive il tipo di un oggetto Picture come restituito da [**IPicture:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)e per descrivere il tipo di immagine nel membro **picType** della struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) che viene passata a [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="e63c2-104">Describe the type of a picture object as returned by [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), as well as to describe the type of picture in the **picType** member of the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure that is passed to [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>



| <span data-ttu-id="e63c2-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="e63c2-105">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="e63c2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e63c2-106">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <span data-ttu-id="e63c2-107"><dt>**PICTYPE \_ Non INIZIALIZZAto**</dt> <dt>(-1)</dt></span><span class="sxs-lookup"><span data-stu-id="e63c2-107"><dt>**PICTYPE\_UNINITIALIZED**</dt> <dt>(-1)</dt></span></span> </dl> | <span data-ttu-id="e63c2-108">Oggetto immagine attualmente non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="e63c2-108">The picture object is currently uninitialized.</span></span> <span data-ttu-id="e63c2-109">Questo valore è valido solo come valore restituito da [**IPicture:: Get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) e non è valido con la struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="e63c2-109">This value is only valid as a return value from [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) and is not valid with the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <span data-ttu-id="e63c2-110"><dt>**PICTYPE \_ NESSUNO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e63c2-110"><dt>**PICTYPE\_NONE**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="e63c2-111">Un nuovo oggetto Picture deve essere creato senza uno stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="e63c2-111">A new picture object is to be created without an initialized state.</span></span> <span data-ttu-id="e63c2-112">Questo valore è valido solo nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="e63c2-112">This value is valid only in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <span data-ttu-id="e63c2-113"><dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e63c2-113"><dt>**PICTYPE\_BITMAP**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="e63c2-114">Il tipo di immagine è una bitmap.</span><span class="sxs-lookup"><span data-stu-id="e63c2-114">The picture type is a bitmap.</span></span> <span data-ttu-id="e63c2-115">Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **BMP** della struttura contiene i parametri di inizializzazione pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e63c2-115">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **bmp** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <span data-ttu-id="e63c2-116"><dt>**PICTYPE \_ METAFILE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e63c2-116"><dt>**PICTYPE\_METAFILE**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="e63c2-117">Il tipo di immagine è un metafile.</span><span class="sxs-lookup"><span data-stu-id="e63c2-117">The picture type is a metafile.</span></span> <span data-ttu-id="e63c2-118">Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **WMF** della struttura contiene i parametri di inizializzazione pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e63c2-118">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **wmf** field of that structure contains the relevant initialization parameters.</span></span><br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <span data-ttu-id="e63c2-119"><dt>**PICTYPE \_ ICONA**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e63c2-119"><dt>**PICTYPE\_ICON**</dt> <dt>3</dt></span></span> </dl>                               | <span data-ttu-id="e63c2-120">Il tipo di immagine è un'icona.</span><span class="sxs-lookup"><span data-stu-id="e63c2-120">The picture type is an icon.</span></span> <span data-ttu-id="e63c2-121">Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **icona** della struttura contiene i parametri di inizializzazione pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e63c2-121">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **icon** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <span data-ttu-id="e63c2-122"><dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e63c2-122"><dt>**PICTYPE\_ENHMETAFILE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="e63c2-123">Il tipo di immagine è un metafile avanzato.</span><span class="sxs-lookup"><span data-stu-id="e63c2-123">The picture type is an enhanced metafile.</span></span> <span data-ttu-id="e63c2-124">Quando questo valore si verifica nella struttura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa che il campo **EMF** della struttura contiene i parametri di inizializzazione pertinenti.</span><span class="sxs-lookup"><span data-stu-id="e63c2-124">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **emf** field of that structure contains the relevant initialization parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e63c2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e63c2-125">Requirements</span></span>



| <span data-ttu-id="e63c2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e63c2-126">Requirement</span></span> | <span data-ttu-id="e63c2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e63c2-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e63c2-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e63c2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e63c2-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e63c2-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e63c2-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e63c2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e63c2-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e63c2-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e63c2-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e63c2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e63c2-133"><dt>OleCtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e63c2-133"><dt>OleCtl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e63c2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e63c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e63c2-135">**Tipo IPicture:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="e63c2-135">**IPicture::get\_Type**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[<span data-ttu-id="e63c2-136">**OleCreatePictureIndirect**</span><span class="sxs-lookup"><span data-stu-id="e63c2-136">**OleCreatePictureIndirect**</span></span>](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[<span data-ttu-id="e63c2-137">**PICTDESC**</span><span class="sxs-lookup"><span data-stu-id="e63c2-137">**PICTDESC**</span></span>](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





