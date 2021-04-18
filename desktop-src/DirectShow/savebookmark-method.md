---
description: Il metodo SaveBookmark salva la posizione del disco corrente e lo stato dell'oggetto MSWebDVD in modo che l'utente possa tornare alla stessa posizione in un secondo momento.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Metodo SaveBookmark (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326988"
---
# <a name="savebookmark-method"></a><span data-ttu-id="d3150-103">Metodo SaveBookmark</span><span class="sxs-lookup"><span data-stu-id="d3150-103">SaveBookmark Method</span></span>

> [!Note]  
> <span data-ttu-id="d3150-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d3150-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d3150-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="d3150-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d3150-106">Il `SaveBookmark` metodo salva la posizione del disco corrente e lo stato dell'oggetto **mswebdvd** in modo che l'utente possa tornare alla stessa posizione in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="d3150-106">The `SaveBookmark` method saves the current disc position and state of the **MSWebDVD** object so the user can return to the same place later.</span></span>

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a><span data-ttu-id="d3150-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3150-107">Return Value</span></span>

<span data-ttu-id="d3150-108">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d3150-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3150-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3150-109">Remarks</span></span>

<span data-ttu-id="d3150-110">Un segnalibro è uno snapshot dello stato corrente del navigatore DVD.</span><span class="sxs-lookup"><span data-stu-id="d3150-110">A bookmark is a snapshot of the DVD Navigator's current state.</span></span> <span data-ttu-id="d3150-111">Sono incluse informazioni quali la posizione di riproduzione sul disco e i flussi audio e immagini secondarie selezionate.</span><span class="sxs-lookup"><span data-stu-id="d3150-111">This includes information such as where it is playing on the disc, and which audio and subpictures streams are selected.</span></span> <span data-ttu-id="d3150-112">Salvando un segnalibro, l'utente può chiudere l'applicazione, arrestare il computer e tornare più tardi per continuare a visualizzare il disco da dove è stato interrotto, con tutte le impostazioni esattamente come prima.</span><span class="sxs-lookup"><span data-stu-id="d3150-112">By saving a bookmark, the user can close the application, shut down the computer, and come back later to continue viewing the disc right where he or she left off, with all settings just as they were before.</span></span> <span data-ttu-id="d3150-113">È possibile salvare un solo segnalibro in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="d3150-113">Only one bookmark can be saved at any given time.</span></span> <span data-ttu-id="d3150-114">Quando si chiama `SaveBookmark` , il segnalibro precedente viene sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="d3150-114">When you call `SaveBookmark`, the old bookmark is overwritten.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3150-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3150-115">Requirements</span></span>



| <span data-ttu-id="d3150-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3150-116">Requirement</span></span> | <span data-ttu-id="d3150-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d3150-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3150-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3150-118">Header</span></span><br/> | <dl> <span data-ttu-id="d3150-119"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3150-119"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3150-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3150-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3150-121">**RestoreBookmark**</span><span class="sxs-lookup"><span data-stu-id="d3150-121">**RestoreBookmark**</span></span>](restorebookmark-method.md)
</dt> </dl>

 

 




