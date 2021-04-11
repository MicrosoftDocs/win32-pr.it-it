---
description: La proprietà FullScreenMode imposta o recupera un valore che indica se la visualizzazione è in modalità schermo intero.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Proprietà FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123555"
---
# <a name="fullscreenmode-property"></a><span data-ttu-id="058a1-103">Proprietà FullScreenMode</span><span class="sxs-lookup"><span data-stu-id="058a1-103">FullScreenMode Property</span></span>

> [!Note]  
> <span data-ttu-id="058a1-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="058a1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="058a1-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="058a1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="058a1-106">La `FullScreenMode` proprietà imposta o recupera un valore che indica se la visualizzazione è in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="058a1-106">The `FullScreenMode` property sets or retrieves a value indicating whether the display is in full-screen mode.</span></span>

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a><span data-ttu-id="058a1-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="058a1-107">Return Value</span></span>

<span data-ttu-id="058a1-108">Restituisce un valore booleano che indica se abilitare o disabilitare la riproduzione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="058a1-108">Returns a Boolean value indicating whether to enable or disable full-screen playback.</span></span>

## <a name="remarks"></a><span data-ttu-id="058a1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="058a1-109">Remarks</span></span>

<span data-ttu-id="058a1-110">Questa proprietà è di lettura/scrittura e il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="058a1-110">This property is read/write with a default value of false.</span></span>



| <span data-ttu-id="058a1-111">Valore</span><span class="sxs-lookup"><span data-stu-id="058a1-111">Value</span></span> | <span data-ttu-id="058a1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="058a1-112">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="058a1-113">true</span><span class="sxs-lookup"><span data-stu-id="058a1-113">true</span></span>  | <span data-ttu-id="058a1-114">Abilitare la riproduzione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="058a1-114">Enable full-screen playback.</span></span> <span data-ttu-id="058a1-115">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="058a1-115">This is the default value</span></span> |
| <span data-ttu-id="058a1-116">false</span><span class="sxs-lookup"><span data-stu-id="058a1-116">false</span></span> | <span data-ttu-id="058a1-117">Disabilitare la riproduzione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="058a1-117">Disable full-screen playback.</span></span>                          |



 

<span data-ttu-id="058a1-118">La modalità schermo intero è disponibile solo quando il controllo MSWebDVD è in esecuzione in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="058a1-118">Full screen mode is only available when the MSWebDVD control is running in windowed mode.</span></span>

 

 



