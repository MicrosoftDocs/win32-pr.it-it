---
title: Funzione ImageList_SetColorTable
description: Imposta la tabella dei colori per un elenco di immagini.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- Controlli di Windows per la funzione ImageList_SetColorTable
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965020"
---
# <a name="imagelist_setcolortable-function"></a><span data-ttu-id="bd661-104">ImageList \_ SetColorTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="bd661-104">ImageList\_SetColorTable function</span></span>

<span data-ttu-id="bd661-105">Imposta la tabella dei colori per un elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="bd661-105">Sets the color table for an image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd661-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd661-106">Syntax</span></span>


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a><span data-ttu-id="bd661-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd661-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd661-108">*himl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd661-108">*himl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd661-109">Tipo: **HIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="bd661-109">Type: **HIMAGELIST**</span></span>

<span data-ttu-id="bd661-110">Handle per l'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="bd661-110">A handle to the image list.</span></span>

</dd> <dt>

<span data-ttu-id="bd661-111">*inizio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd661-111">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd661-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="bd661-112">Type: **int**</span></span>

<span data-ttu-id="bd661-113">Indice della tabella dei colori in base zero che specifica la prima voce della tabella dei colori da impostare.</span><span class="sxs-lookup"><span data-stu-id="bd661-113">A zero-based color table index that specifies the first color table entry to set.</span></span>

</dd> <dt>

<span data-ttu-id="bd661-114">*Len* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd661-114">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd661-115">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="bd661-115">Type: **int**</span></span>

<span data-ttu-id="bd661-116">Numero di voci della tabella dei colori da impostare.</span><span class="sxs-lookup"><span data-stu-id="bd661-116">The number of color table entries to set.</span></span>

</dd> <dt>

<span data-ttu-id="bd661-117">*prgb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd661-117">*prgb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd661-118">Tipo: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _</span><span class="sxs-lookup"><span data-stu-id="bd661-118">Type: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\** _</span></span>

<span data-ttu-id="bd661-119">Puntatore a una matrice di strutture _len \* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) contenenti nuove informazioni sui colori per la tabella dei colori della DIB.</span><span class="sxs-lookup"><span data-stu-id="bd661-119">A pointer to an array of _len\* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures containing new color information for the color table of the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd661-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd661-120">Return value</span></span>

<span data-ttu-id="bd661-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="bd661-121">Type: **int**</span></span>

<span data-ttu-id="bd661-122">Se la funzione ha esito positivo, restituisce il numero di voci della tabella dei colori impostate dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="bd661-122">If the function succeeds, it returns the number of color table entries set by the function.</span></span> <span data-ttu-id="bd661-123">Se la funzione ha esito negativo, il valore restituito è minore o uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="bd661-123">If the function fails, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd661-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd661-124">Remarks</span></span>

<span data-ttu-id="bd661-125">Solo gli elenchi di immagini creati con il flag [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) o [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) hanno tabelle dei colori.</span><span class="sxs-lookup"><span data-stu-id="bd661-125">Only image lists created with the [**ILC\_COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) or [**ILC\_COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) flag have color tables.</span></span> <span data-ttu-id="bd661-126">La tabella dei colori di un elenco di immagini di questo tipo viene in genere impostata automaticamente copiando la tabella dei colori della prima immagine aggiunta all'elenco (ad esempio, tramite la funzione di [**\_ aggiunta ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) se l'immagine è una DIB.</span><span class="sxs-lookup"><span data-stu-id="bd661-126">The color table of such an image list is typically set automatically by copying the color table of the first image added to the list (for example, through the [**ImageList\_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) function) if that image is a DIB.</span></span> <span data-ttu-id="bd661-127">Se la prima immagine aggiunta all'elenco di immagini non è una DIB, viene usata la tabella dei colori della tavolozza mezzitoni per gli elenchi di immagini **\_ COLOR8 di ILC** e viene usata la tabella dei colori VGA per **ILC \_ COLOR4**.</span><span class="sxs-lookup"><span data-stu-id="bd661-127">If the first image added to the image list is not a DIB, then the color table of the halftone palette is used for **ILC\_COLOR8** image lists and the VGA color table is used for **ILC\_COLOR4**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd661-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd661-128">Requirements</span></span>



| <span data-ttu-id="bd661-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd661-129">Requirement</span></span> | <span data-ttu-id="bd661-130">Valore</span><span class="sxs-lookup"><span data-stu-id="bd661-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd661-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd661-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bd661-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd661-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="bd661-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd661-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bd661-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd661-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bd661-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bd661-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd661-136"><dt>Comctl32.dll (versione 3,51 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bd661-136"><dt>Comctl32.dll (version 3.51 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd661-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd661-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd661-138">[Tabella colori](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="bd661-138">[Color Table](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span></span>
</dt> </dl>

 

