---
title: Media. getMarkerTime, metodo
description: Il metodo getMarkerTime recupera l'ora del marcatore in corrispondenza dell'indice specificato.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- Metodo getMarkerTime Windows Media Player
- Metodo getMarkerTime Windows Media Player, classe media
- Media class Media Player Windows, metodo getMarkerTime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331865"
---
# <a name="mediagetmarkertime-method"></a><span data-ttu-id="45570-106">Media. getMarkerTime, metodo</span><span class="sxs-lookup"><span data-stu-id="45570-106">Media.getMarkerTime method</span></span>

<span data-ttu-id="45570-107">Il metodo **getMarkerTime** recupera l'ora del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="45570-107">The **getMarkerTime** method retrieves the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="45570-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45570-108">Syntax</span></span>


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="45570-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="45570-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45570-110">*markerNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45570-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45570-111">**Numero** (**Long**) che specifica l'indice del marcatore.</span><span class="sxs-lookup"><span data-stu-id="45570-111">**Number** (**long**) specifying the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45570-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45570-112">Return value</span></span>

<span data-ttu-id="45570-113">Questo metodo restituisce un **numero** (**Double**) che specifica la posizione del marcatore in secondi dall'inizio della clip.</span><span class="sxs-lookup"><span data-stu-id="45570-113">This method returns a **Number** (**double**) specifying the location of the marker in seconds from the beginning of the clip.</span></span>

## <a name="remarks"></a><span data-ttu-id="45570-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="45570-114">Remarks</span></span>

<span data-ttu-id="45570-115">Questo metodo restituisce **null** se il marcatore specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="45570-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="45570-116">Alcuni elementi multimediali digitali non contengono marcatori.</span><span class="sxs-lookup"><span data-stu-id="45570-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="45570-117">Usare **markerCount** per verificare il numero di marcatori presenti nella clip corrente.</span><span class="sxs-lookup"><span data-stu-id="45570-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="45570-118">I numeri di indice del marcatore iniziano da 1.</span><span class="sxs-lookup"><span data-stu-id="45570-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="45570-119">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="45570-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="45570-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="45570-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="45570-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="45570-121">Examples</span></span>

<span data-ttu-id="45570-122">Nell'esempio JScript seguente viene usato il *supporto*. **getMarkerTime** per inserire un elemento textarea HTML denominato MTIMES con la posizione di ogni marcatore.</span><span class="sxs-lookup"><span data-stu-id="45570-122">The following JScript example uses *Media*.**getMarkerTime** to fill an HTML TEXTAREA element named MTIMES with the location of each marker.</span></span> <span data-ttu-id="45570-123">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="45570-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="45570-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45570-124">Requirements</span></span>



| <span data-ttu-id="45570-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="45570-125">Requirement</span></span> | <span data-ttu-id="45570-126">Valore</span><span class="sxs-lookup"><span data-stu-id="45570-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45570-127">Versione</span><span class="sxs-lookup"><span data-stu-id="45570-127">Version</span></span><br/> | <span data-ttu-id="45570-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="45570-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="45570-129">DLL</span><span class="sxs-lookup"><span data-stu-id="45570-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="45570-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45570-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45570-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45570-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45570-132">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="45570-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="45570-133">**Media. getmarkname**</span><span class="sxs-lookup"><span data-stu-id="45570-133">**Media.getMarkerName**</span></span>](media-getmarkername.md)
</dt> <dt>

[<span data-ttu-id="45570-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="45570-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="45570-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="45570-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="45570-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="45570-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





