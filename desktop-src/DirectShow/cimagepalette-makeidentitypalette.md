---
description: Il metodo MakeIdentityPalette tenta di creare un &\# 0034; Identity palette, &\# 0034; definito come uno che esegue il mapping direttamente alla tavolozza selezionata nel dispositivo di visualizzazione.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Metodo CImagePalette. MakeIdentityPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325067"
---
# <a name="cimagepalettemakeidentitypalette-method"></a><span data-ttu-id="14e32-103">CImagePalette. MakeIdentityPalette, metodo</span><span class="sxs-lookup"><span data-stu-id="14e32-103">CImagePalette.MakeIdentityPalette method</span></span>

<span data-ttu-id="14e32-104">Il `MakeIdentityPalette` metodo tenta di creare una "tavolozza di identità", definita come uno che esegue il mapping direttamente alla tavolozza selezionata nel dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="14e32-104">The `MakeIdentityPalette` method attempts to make an "identity palette," defined as one that maps directly to the palette selected in the display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14e32-105">Syntax</span></span>


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="14e32-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14e32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e32-107">*Pente*</span><span class="sxs-lookup"><span data-stu-id="14e32-107">*pEntry*</span></span> 
</dt> <dd>

<span data-ttu-id="14e32-108">Puntatore a una matrice di voci della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="14e32-108">Pointer to an array of palette entries.</span></span>

</dd> <dt>

<span data-ttu-id="14e32-109">*iColours*</span><span class="sxs-lookup"><span data-stu-id="14e32-109">*iColours*</span></span> 
</dt> <dd>

<span data-ttu-id="14e32-110">Numero di voci della tavolozza in *pente*.</span><span class="sxs-lookup"><span data-stu-id="14e32-110">Number of palette entries in *pEntry*.</span></span>

</dd> <dt>

<span data-ttu-id="14e32-111">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="14e32-111">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="14e32-112">Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI.</span><span class="sxs-lookup"><span data-stu-id="14e32-112">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="14e32-113">Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="14e32-113">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e32-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14e32-114">Return value</span></span>

<span data-ttu-id="14e32-115">Restituisce \_ OK se l'operazione ha esito positivo o \_ false se non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="14e32-115">Returns S\_OK if successful or S\_FALSE if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e32-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="14e32-116">Remarks</span></span>

<span data-ttu-id="14e32-117">Questo metodo confronta le voci riservate nella tavolozza di sistema con le voci corrispondenti nell' *Array.*</span><span class="sxs-lookup"><span data-stu-id="14e32-117">This method compares the reserved entries in the system palette against the corresponding entries in the *pEntry* array.</span></span> <span data-ttu-id="14e32-118">Se corrispondono esattamente, il metodo imposta il flag PC \_ nocollapse nelle voci della tavolozza rimanenti (non riservate) in *pente*.</span><span class="sxs-lookup"><span data-stu-id="14e32-118">If they match exactly, the method sets the PC\_NOCOLLAPSE flag in the remaining (non-reserved) palette entries in *pEntry*.</span></span> <span data-ttu-id="14e32-119">Questo flag impedisce a GDI di provare a eseguire il mapping delle voci della tavolozza logica alle voci della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="14e32-119">This flag prevents GDI from trying map logical palette entries to system palette entries.</span></span>

<span data-ttu-id="14e32-120">Il metodo [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="14e32-120">The [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e32-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14e32-121">Requirements</span></span>



| <span data-ttu-id="14e32-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14e32-122">Requirement</span></span> | <span data-ttu-id="14e32-123">Valore</span><span class="sxs-lookup"><span data-stu-id="14e32-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14e32-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14e32-124">Header</span></span><br/>  | <dl> <span data-ttu-id="14e32-125"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14e32-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="14e32-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="14e32-126">Library</span></span><br/> | <dl> <span data-ttu-id="14e32-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="14e32-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e32-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14e32-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e32-129">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="14e32-129">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




