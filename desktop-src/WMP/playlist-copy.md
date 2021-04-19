---
title: PLAYLIST. Copy
description: Il metodo Copy avvia un'operazione di copia dal CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- PLAYLIST. copiare Media Player Windows
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328046"
---
# <a name="playlistcopy"></a><span data-ttu-id="2a8f3-104">PLAYLIST. Copy</span><span class="sxs-lookup"><span data-stu-id="2a8f3-104">PLAYLIST.copy</span></span>

<span data-ttu-id="2a8f3-105">Il metodo **Copy** avvia un'operazione di copia dal CD.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-105">The **copy** method begins a copy operation from the CD.</span></span>

``` syntax
        elementID.copy()
```

## <a name="parameters"></a><span data-ttu-id="2a8f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a8f3-106">Parameters</span></span>

<span data-ttu-id="2a8f3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a8f3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a8f3-108">Return Value</span></span>

<span data-ttu-id="2a8f3-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a8f3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a8f3-110">Remarks</span></span>

<span data-ttu-id="2a8f3-111">Questo metodo copia solo gli elementi selezionati nella playlist e funziona allo stesso modo del riquadro **copia da CD** nella modalità completa di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-111">This method copies only the checked items in the playlist, and works the same way as in the **Copy from CD** pane in the full mode of Windows Media Player.</span></span> <span data-ttu-id="2a8f3-112">Per il corretto funzionamento di questo metodo, è necessario che sia presente un CD nell'unità CD.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-112">For this method to work, a CD must be in the CD drive.</span></span> <span data-ttu-id="2a8f3-113">Impostare l'attributo **checkboxesVisible** su true per consentire agli utenti di selezionare singoli elementi in un CD prima della copia.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-113">Set the **checkboxesVisible** attribute to true to allow users to select individual items on a CD before copying.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8f3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a8f3-114">Requirements</span></span>



| <span data-ttu-id="2a8f3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a8f3-115">Requirement</span></span> | <span data-ttu-id="2a8f3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2a8f3-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2a8f3-117">Versione</span><span class="sxs-lookup"><span data-stu-id="2a8f3-117">Version</span></span><br/> | <span data-ttu-id="2a8f3-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="2a8f3-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a8f3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a8f3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a8f3-120">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="2a8f3-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="2a8f3-121">**PLAYLIST. abortCopy**</span><span class="sxs-lookup"><span data-stu-id="2a8f3-121">**PLAYLIST.abortCopy**</span></span>](playlist-abortcopy.md)
</dt> <dt>

[<span data-ttu-id="2a8f3-122">**PLAYLIST. copia**</span><span class="sxs-lookup"><span data-stu-id="2a8f3-122">**PLAYLIST.copying**</span></span>](playlist-copying.md)
</dt> </dl>

 

 





