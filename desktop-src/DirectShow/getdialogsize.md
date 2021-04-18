---
description: La funzione GetDialogSize recupera le dimensioni di una finestra di dialogo della risorsa.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Funzione GetDialogSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330937"
---
# <a name="getdialogsize-function"></a><span data-ttu-id="0fe4e-103">GetDialogSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="0fe4e-103">GetDialogSize function</span></span>

<span data-ttu-id="0fe4e-104">La funzione **GetDialogSize** recupera le dimensioni di una finestra di dialogo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-104">The **GetDialogSize** function retrieves the size of a resource dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe4e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fe4e-105">Syntax</span></span>


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a><span data-ttu-id="0fe4e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fe4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fe4e-107">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="0fe4e-107">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="0fe4e-108">Identificatore della risorsa della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-108">Dialog box resource identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0fe4e-109">*pDlgProc*</span><span class="sxs-lookup"><span data-stu-id="0fe4e-109">*pDlgProc*</span></span> 
</dt> <dd>

<span data-ttu-id="0fe4e-110">Puntatore alla routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-110">Pointer to the dialog box procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0fe4e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fe4e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fe4e-112">Valore passato al messaggio WM \_ INITDIALOG inviato alla finestra di dialogo temporanea subito dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-112">Value passed in the WM\_INITDIALOG message sent to the temporary dialog box just after it is created.</span></span>

</dd> <dt>

<span data-ttu-id="0fe4e-113">*pResult*</span><span class="sxs-lookup"><span data-stu-id="0fe4e-113">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="0fe4e-114">Puntatore a una struttura di **dimensioni** che riceve le dimensioni della finestra di dialogo, in pixel dello schermo.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-114">Pointer to a **SIZE** structure that receives the dimensions of the dialog box, in screen pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fe4e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fe4e-115">Return value</span></span>

<span data-ttu-id="0fe4e-116">Restituisce **true** se la risorsa della finestra di dialogo è stata trovata; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="0fe4e-116">Returns **TRUE** if the dialog box resource was found, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe4e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fe4e-117">Remarks</span></span>

<span data-ttu-id="0fe4e-118">Le pagine delle proprietà possono usare questa funzione per restituire le dimensioni di visualizzazione effettive necessarie.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-118">Property pages can use this function to return the actual display size they require.</span></span> <span data-ttu-id="0fe4e-119">La maggior parte delle pagine delle proprietà sono finestre di dialogo e, di conseguenza, i modelli di finestra di dialogo archiviati nei file di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-119">Most property pages are dialog boxes and, as such, have dialog box templates stored in resource files.</span></span> <span data-ttu-id="0fe4e-120">I modelli usano unità della finestra di dialogo che non eseguono il mapping direttamente sui pixel dello schermo.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-120">Templates use dialog box units that do not map directly onto screen pixels.</span></span> <span data-ttu-id="0fe4e-121">Tuttavia, la funzione [**GetPageInfo**](cbasepropertypage-getpageinfo.md) della pagina delle proprietà deve restituire le dimensioni di visualizzazione effettive in pixel.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-121">However, a property page's [**GetPageInfo**](cbasepropertypage-getpageinfo.md) function must return the actual display size in pixels.</span></span> <span data-ttu-id="0fe4e-122">La pagina delle proprietà può chiamare `GetDialogSize` per calcolare le dimensioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-122">The property page can call `GetDialogSize` to calculate the display size.</span></span>

<span data-ttu-id="0fe4e-123">Questa funzione crea un'istanza temporanea della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-123">This function creates a temporary instance of the dialog box.</span></span> <span data-ttu-id="0fe4e-124">Per evitare che la finestra di dialogo venga visualizzata sullo schermo, il modello della finestra di dialogo nel file di risorse non deve avere una \_ Proprietà WS Visible.</span><span class="sxs-lookup"><span data-stu-id="0fe4e-124">To avoid having the dialog box appear on the screen, the dialog box template in the resource file should not have a WS\_VISIBLE property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe4e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fe4e-125">Requirements</span></span>



| <span data-ttu-id="0fe4e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fe4e-126">Requirement</span></span> | <span data-ttu-id="0fe4e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0fe4e-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe4e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fe4e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0fe4e-129"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe4e-129"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0fe4e-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fe4e-130">Library</span></span><br/> | <dl> <span data-ttu-id="0fe4e-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0fe4e-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe4e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fe4e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe4e-133">Funzioni di supporto della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0fe4e-133">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




