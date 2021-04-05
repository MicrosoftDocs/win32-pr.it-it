---
description: La proprietà DVDDirectory imposta o recupera la directory corrente del volume DVD corrente.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Proprietà DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876573"
---
# <a name="dvddirectory-property"></a><span data-ttu-id="3fab3-103">Proprietà DVDDirectory</span><span class="sxs-lookup"><span data-stu-id="3fab3-103">DVDDirectory Property</span></span>

> [!Note]  
> <span data-ttu-id="3fab3-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3fab3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3fab3-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="3fab3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3fab3-106">La `DVDDirectory` proprietà imposta o recupera la directory corrente del volume DVD corrente.</span><span class="sxs-lookup"><span data-stu-id="3fab3-106">The `DVDDirectory` property sets or retrieves the current directory of the current DVD volume.</span></span>

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a><span data-ttu-id="3fab3-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fab3-107">Return Value</span></span>

<span data-ttu-id="3fab3-108">Restituisce un valore stringa che indica il percorso della directory radice DVD.</span><span class="sxs-lookup"><span data-stu-id="3fab3-108">Returns a string value indicating the path to the DVD root directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fab3-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fab3-109">Remarks</span></span>

<span data-ttu-id="3fab3-110">Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3fab3-110">This property is read/write with no default value.</span></span> <span data-ttu-id="3fab3-111">Utilizzare questo metodo per impostare il percorso radice quando è presente più di un'unità DVD in un sistema.</span><span class="sxs-lookup"><span data-stu-id="3fab3-111">Use this method to set the root path when there is more than one DVD drive on a system.</span></span> <span data-ttu-id="3fab3-112">Quando nel sistema è presente una sola unità e la lettera di unità è superiore a "C", l'oggetto MSWebDVD lo trova automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3fab3-112">When there is only one drive on the system and its drive letter is higher than "C", the MSWebDVD object finds it automatically.</span></span> <span data-ttu-id="3fab3-113">Per un disco DVD-Video standard, il percorso radice deve includere la directory video di Servizi terminal \_ :</span><span class="sxs-lookup"><span data-stu-id="3fab3-113">For a standard DVD-Video disc, the root path should include the ts\_video directory:</span></span>


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



<span data-ttu-id="3fab3-114">Alcuni volumi DVD possono avere un video in una directory denominata qualcosa di diverso da "video \_ TS".</span><span class="sxs-lookup"><span data-stu-id="3fab3-114">Some DVD volumes may have their video in a directory named something other than "video\_ts."</span></span> <span data-ttu-id="3fab3-115">L'idea generale è che un "volume DVD" aggiuntivo (il set di. IFO.</span><span class="sxs-lookup"><span data-stu-id="3fab3-115">The general idea is that an additional "DVD volume" (the set of .IFO.</span></span> <span data-ttu-id="3fab3-116">VOB, e. I file BUP normalmente archiviati nella \_ directory di Servizi terminal video possono essere inseriti in una sottodirectory del disco. Cambiando la radice in modo che punti a questa directory, MSWebDVD funzionerà su questo volume DVD separato.</span><span class="sxs-lookup"><span data-stu-id="3fab3-116">VOB, and .BUP files that would normally be stored in the VIDEO\_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume.</span></span> <span data-ttu-id="3fab3-117">Sarà disponibile un nuovo set di menu, titoli e così via, indipendentemente dai titoli nella radice del VIDEO \_ TS, che non sarà più accessibile.</span><span class="sxs-lookup"><span data-stu-id="3fab3-117">A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO\_TS root, which will no longer be accessible.</span></span> <span data-ttu-id="3fab3-118">Tali directory sono denominate "directory nascoste".</span><span class="sxs-lookup"><span data-stu-id="3fab3-118">Such directories are called "hidden directories."</span></span> <span data-ttu-id="3fab3-119">Nell'esempio seguente viene illustrato come impostare una directory nascosta come radice, dove "hidden" è un segnaposto per qualsiasi nome assegnato alla directory dagli autori del disco.</span><span class="sxs-lookup"><span data-stu-id="3fab3-119">The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.</span></span>


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



