---
title: Media. markerCount
description: La proprietà markerCount Recupera il numero di marcatori nell'elemento multimediale.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media Player Windows Media. markerCount
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329307"
---
# <a name="mediamarkercount"></a><span data-ttu-id="a3502-104">Media. markerCount</span><span class="sxs-lookup"><span data-stu-id="a3502-104">Media.markerCount</span></span>

<span data-ttu-id="a3502-105">La proprietà **markerCount** Recupera il numero di marcatori nell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a3502-105">The **markerCount** property retrieves the number of markers in the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3502-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3502-106">Syntax</span></span>

<span data-ttu-id="a3502-107">*Player*. *currentMedia*. **markerCount**</span><span class="sxs-lookup"><span data-stu-id="a3502-107">*player*.*currentMedia*.**markerCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a3502-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a3502-108">Possible Values</span></span>

<span data-ttu-id="a3502-109">Questa proprietà è un **numero** di sola lettura (**Long**) che specifica il numero di marcatori nel file.</span><span class="sxs-lookup"><span data-stu-id="a3502-109">This property is a read-only **Number** (**long**) specifying the number of markers in the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3502-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3502-110">Remarks</span></span>

<span data-ttu-id="a3502-111">Questa proprietà restituisce zero se un file non ha marcatori o se l'elemento multimediale non è uguale a *Player*. **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="a3502-111">This property returns zero if a file has no markers, or if the media item is not the same as *Player*.**currentMedia**.</span></span>

<span data-ttu-id="a3502-112">I numeri degli indicatori iniziano da 1.</span><span class="sxs-lookup"><span data-stu-id="a3502-112">Marker numbers start at 1.</span></span>

<span data-ttu-id="a3502-113">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="a3502-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="a3502-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a3502-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a3502-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="a3502-115">Examples</span></span>

<span data-ttu-id="a3502-116">Nell'esempio JScript seguente viene usato il *supporto*. **markerCount** per recuperare il numero di marcatori nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="a3502-116">The following JScript example uses *Media*.**markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="a3502-117">Tale valore viene quindi utilizzato come limite superiore per una struttura di ciclo, che scorre l'elenco dei marcatori per recuperare ogni nome del marcatore.</span><span class="sxs-lookup"><span data-stu-id="a3502-117">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name.</span></span> <span data-ttu-id="a3502-118">Un elemento TEXTAREA HTML denominato MNAMES Visualizza i nomi dei marcatori nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="a3502-118">An HTML TEXTAREA element named MNAMES displays the names of the markers in the current media item.</span></span> <span data-ttu-id="a3502-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a3502-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="a3502-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3502-120">Requirements</span></span>



| <span data-ttu-id="a3502-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3502-121">Requirement</span></span> | <span data-ttu-id="a3502-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a3502-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3502-123">Versione</span><span class="sxs-lookup"><span data-stu-id="a3502-123">Version</span></span><br/> | <span data-ttu-id="a3502-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a3502-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a3502-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a3502-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3502-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3502-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3502-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3502-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3502-128">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="a3502-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="a3502-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="a3502-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="a3502-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a3502-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a3502-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a3502-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





