---
description: Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Struttura DEVICEDIALOGDATA (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529155"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="80c83-103">Struttura DEVICEDIALOGDATA</span><span class="sxs-lookup"><span data-stu-id="80c83-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="80c83-104">Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80c83-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80c83-105">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a><span data-ttu-id="80c83-106">Members</span><span class="sxs-lookup"><span data-stu-id="80c83-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="80c83-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="80c83-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="80c83-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="80c83-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="80c83-109">Specifica la dimensione in byte della struttura.</span><span class="sxs-lookup"><span data-stu-id="80c83-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="80c83-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="80c83-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="80c83-111">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="80c83-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="80c83-112">Specifica l'handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="80c83-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="80c83-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="80c83-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="80c83-114">Tipo: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _</span><span class="sxs-lookup"><span data-stu-id="80c83-114">Type: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\** _</span></span>

</dd> <dd>

<span data-ttu-id="80c83-115">Punta a un'interfaccia [_ *IWiaItem* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80c83-115">Points to an [_ *IWiaItem*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="80c83-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="80c83-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="80c83-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="80c83-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="80c83-118">Specifica un set di flag che controllano l'operazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="80c83-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="80c83-119">Può essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="80c83-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="80c83-120">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="80c83-120">Flag</span></span>                                 | <span data-ttu-id="80c83-121">Significato</span><span class="sxs-lookup"><span data-stu-id="80c83-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c83-122">0</span><span class="sxs-lookup"><span data-stu-id="80c83-122">0</span></span>                                    | <span data-ttu-id="80c83-123">Comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="80c83-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="80c83-124">\_ \_ immagine singola della finestra di dialogo del dispositivo WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="80c83-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="80c83-125">Limitare la selezione delle immagini a una singola immagine nella finestra di dialogo acquisizione immagine del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80c83-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="80c83-126">\_finestra di dialogo del dispositivo WIA usare l' \_ \_ \_ \_ interfaccia utente comune</span><span class="sxs-lookup"><span data-stu-id="80c83-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="80c83-127">Utilizzare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="80c83-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="80c83-128">Se l'interfaccia utente del sistema non è disponibile, viene utilizzata l'interfaccia utente del fornitore.</span><span class="sxs-lookup"><span data-stu-id="80c83-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="80c83-129">Se nessuna delle due interfacce è disponibile, la funzione restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="80c83-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="80c83-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="80c83-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="80c83-131">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="80c83-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="80c83-132">Specifica il tipo di dati che l'immagine deve rappresentare.</span><span class="sxs-lookup"><span data-stu-id="80c83-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="80c83-133">Per un elenco di valori per finalità immagine, vedere [**costanti per finalità di immagine**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="80c83-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="80c83-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="80c83-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="80c83-135">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="80c83-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="80c83-136">Riceve il numero di elementi nella matrice indicata dal parametro **ppWiaItem** .</span><span class="sxs-lookup"><span data-stu-id="80c83-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="80c83-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="80c83-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="80c83-138">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="80c83-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="80c83-139">Riceve l'indirizzo di una matrice di puntatori alle interfacce [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="80c83-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80c83-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80c83-140">Requirements</span></span>



| <span data-ttu-id="80c83-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c83-141">Requirement</span></span> | <span data-ttu-id="80c83-142">Valore</span><span class="sxs-lookup"><span data-stu-id="80c83-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="80c83-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80c83-143">Minimum supported client</span></span><br/> | <span data-ttu-id="80c83-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80c83-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="80c83-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80c83-145">Minimum supported server</span></span><br/> | <span data-ttu-id="80c83-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80c83-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="80c83-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80c83-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="80c83-148"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="80c83-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




