---
description: 'Struttura DEVICEDIALOGDATA: definisce i dati necessari per chiamare un dialogo del dispositivo.'
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Struttura DEVICEDIALOGDATA (Wiadefd.h)
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
ms.openlocfilehash: ad7b08f5396a7a6e9b1f74df3dd409303b2d548d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104269"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="3777d-103">Struttura DEVICEDIALOGDATA</span><span class="sxs-lookup"><span data-stu-id="3777d-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="3777d-104">Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3777d-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="3777d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3777d-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="3777d-106">Members</span><span class="sxs-lookup"><span data-stu-id="3777d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3777d-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="3777d-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="3777d-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3777d-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3777d-109">Specifica le dimensioni della struttura in byte.</span><span class="sxs-lookup"><span data-stu-id="3777d-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3777d-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="3777d-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="3777d-111">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="3777d-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="3777d-112">Specifica l'handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="3777d-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="3777d-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="3777d-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="3777d-114">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span><span class="sxs-lookup"><span data-stu-id="3777d-114">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span></span>

</dd> <dd>

<span data-ttu-id="3777d-115">Punta a [**un'interfaccia IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3777d-115">Points to an [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="3777d-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="3777d-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="3777d-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3777d-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3777d-118">Specifica un set di flag che controllano l'operazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="3777d-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="3777d-119">Può essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3777d-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="3777d-120">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="3777d-120">Flag</span></span>                                 | <span data-ttu-id="3777d-121">Significato</span><span class="sxs-lookup"><span data-stu-id="3777d-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3777d-122">0</span><span class="sxs-lookup"><span data-stu-id="3777d-122">0</span></span>                                    | <span data-ttu-id="3777d-123">Comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="3777d-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="3777d-124">IMMAGINE SINGOLA \_ DELLA FINESTRA DI DIALOGO DEL \_ \_ DISPOSITIVO \_ WIA</span><span class="sxs-lookup"><span data-stu-id="3777d-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="3777d-125">Limitare la selezione dell'immagine a una singola immagine nella finestra di dialogo di acquisizione dell'immagine del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3777d-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="3777d-126">FINESTRA DI DIALOGO DEL DISPOSITIVO WIA \_ \_ USA \_ \_ L'INTERFACCIA \_ UTENTE COMUNE</span><span class="sxs-lookup"><span data-stu-id="3777d-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="3777d-127">Usare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="3777d-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="3777d-128">Se l'interfaccia utente del sistema non è disponibile, viene usata l'interfaccia utente del fornitore.</span><span class="sxs-lookup"><span data-stu-id="3777d-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="3777d-129">Se nessuna delle due interfaccia utente è disponibile, la funzione restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="3777d-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3777d-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="3777d-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="3777d-131">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="3777d-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="3777d-132">Specifica il tipo di dati che l'immagine deve rappresentare.</span><span class="sxs-lookup"><span data-stu-id="3777d-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="3777d-133">Per un elenco dei valori di finalità dell'immagine, vedere [**Costanti finalità immagine.**](-wia-imageintentconstants.md)</span><span class="sxs-lookup"><span data-stu-id="3777d-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3777d-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="3777d-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="3777d-135">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="3777d-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="3777d-136">Riceve il numero di elementi nella matrice indicata dal **parametro ppWiaItem.**</span><span class="sxs-lookup"><span data-stu-id="3777d-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3777d-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="3777d-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="3777d-138">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="3777d-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="3777d-139">Riceve l'indirizzo di una matrice di puntatori [**alle interfacce IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)</span><span class="sxs-lookup"><span data-stu-id="3777d-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3777d-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3777d-140">Requirements</span></span>



| <span data-ttu-id="3777d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3777d-141">Requirement</span></span> | <span data-ttu-id="3777d-142">Valore</span><span class="sxs-lookup"><span data-stu-id="3777d-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3777d-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3777d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3777d-144">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3777d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3777d-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3777d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3777d-146">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3777d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3777d-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3777d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3777d-148"><dt>Wiadefd.h</dt></span><span class="sxs-lookup"><span data-stu-id="3777d-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




