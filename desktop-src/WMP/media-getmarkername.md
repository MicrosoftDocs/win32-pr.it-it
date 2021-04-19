---
title: Media. getmarkname, metodo
description: Il metodo getmarkname Recupera il nome del marcatore in corrispondenza dell'indice specificato.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- Metodo getmarkname Media Player Windows
- Metodo getmarkname Media Player Windows, classe media
- Media class Media Player Windows, metodo getmarkname
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332545"
---
# <a name="mediagetmarkername-method"></a><span data-ttu-id="93798-106">Media. getmarkname, metodo</span><span class="sxs-lookup"><span data-stu-id="93798-106">Media.getMarkerName method</span></span>

<span data-ttu-id="93798-107">Il metodo **Getmarkname** Recupera il nome del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="93798-107">The **getMarkerName** method retrieves the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="93798-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93798-108">Syntax</span></span>


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="93798-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="93798-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93798-110">*markerNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93798-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93798-111">**Numero** (**Long**) che specifica un indice del marcatore.</span><span class="sxs-lookup"><span data-stu-id="93798-111">**Number** (**long**) specifying a marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93798-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93798-112">Return value</span></span>

<span data-ttu-id="93798-113">Questo metodo restituisce una **stringa**.</span><span class="sxs-lookup"><span data-stu-id="93798-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93798-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="93798-114">Remarks</span></span>

<span data-ttu-id="93798-115">Questo metodo restituisce **null** se il marcatore specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="93798-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="93798-116">Alcuni elementi multimediali digitali non contengono marcatori.</span><span class="sxs-lookup"><span data-stu-id="93798-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="93798-117">Usare **markerCount** per verificare il numero di marcatori presenti nella clip corrente.</span><span class="sxs-lookup"><span data-stu-id="93798-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="93798-118">I numeri di indice del marcatore iniziano da 1.</span><span class="sxs-lookup"><span data-stu-id="93798-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="93798-119">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="93798-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="93798-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="93798-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="93798-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="93798-121">Examples</span></span>

<span data-ttu-id="93798-122">Nell'esempio JScript seguente viene usato il *supporto*. **Getmarkername** per inserire un elemento textarea HTML denominato MNAMES con i nomi dei marcatori nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="93798-122">The following JScript example uses *Media*.**getMarkerName** to fill an HTML TEXTAREA element named MNAMES with the names of the markers in the current media item.</span></span> <span data-ttu-id="93798-123">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="93798-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="93798-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93798-124">Requirements</span></span>



| <span data-ttu-id="93798-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93798-125">Requirement</span></span> | <span data-ttu-id="93798-126">Valore</span><span class="sxs-lookup"><span data-stu-id="93798-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93798-127">Versione</span><span class="sxs-lookup"><span data-stu-id="93798-127">Version</span></span><br/> | <span data-ttu-id="93798-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="93798-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="93798-129">DLL</span><span class="sxs-lookup"><span data-stu-id="93798-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="93798-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93798-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93798-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93798-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93798-132">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="93798-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="93798-133">**Media. getMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="93798-133">**Media.getMarkerTime**</span></span>](media-getmarkertime.md)
</dt> <dt>

[<span data-ttu-id="93798-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="93798-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="93798-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="93798-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="93798-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="93798-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





