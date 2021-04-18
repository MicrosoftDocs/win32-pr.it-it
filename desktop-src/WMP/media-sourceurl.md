---
title: Media. sourceURL
description: La proprietà sourceURL recupera l'URL dell'elemento multimediale.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media Player Windows Media. sourceURL
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330360"
---
# <a name="mediasourceurl"></a><span data-ttu-id="c9791-104">Media. sourceURL</span><span class="sxs-lookup"><span data-stu-id="c9791-104">Media.sourceURL</span></span>

<span data-ttu-id="c9791-105">La proprietà **sourceURL** recupera l'URL dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="c9791-105">The **sourceURL** property retrieves the URL of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9791-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9791-106">Syntax</span></span>

<span data-ttu-id="c9791-107">*Player*. *currentMedia*. sourceURL</span><span class="sxs-lookup"><span data-stu-id="c9791-107">*player*.*currentMedia*.sourceURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="c9791-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c9791-108">Possible Values</span></span>

<span data-ttu-id="c9791-109">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c9791-109">This property is a read-only **String**.</span></span>

## <a name="examples"></a><span data-ttu-id="c9791-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="c9791-110">Examples</span></span>

<span data-ttu-id="c9791-111">Nell'esempio JScript seguente viene usato il *supporto*. **sourceURL** recuperare l'URL del primo elemento multimediale nella playlist di esempio; l'URL dell'elemento multimediale viene quindi assegnato alla proprietà **URL** oggetto Player.</span><span class="sxs-lookup"><span data-stu-id="c9791-111">The following JScript example uses *Media*.**sourceURL** to retrieve the URL of the first media item in the sample playlist; the URL of the media item is then assigned to the player object **URL** property.</span></span> <span data-ttu-id="c9791-112">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c9791-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="c9791-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9791-113">Requirements</span></span>



| <span data-ttu-id="c9791-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9791-114">Requirement</span></span> | <span data-ttu-id="c9791-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c9791-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9791-116">Versione</span><span class="sxs-lookup"><span data-stu-id="c9791-116">Version</span></span><br/> | <span data-ttu-id="c9791-117">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c9791-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c9791-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c9791-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9791-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9791-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9791-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9791-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9791-121">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="c9791-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





