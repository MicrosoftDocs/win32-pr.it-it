---
description: La proprietà SubpictureOn imposta o recupera lo stato della sottoimmagine corrente (on o off).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Proprietà SubpictureOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317836"
---
# <a name="subpictureon-property"></a><span data-ttu-id="86bee-103">Proprietà SubpictureOn</span><span class="sxs-lookup"><span data-stu-id="86bee-103">SubpictureOn Property</span></span>

> [!Note]  
> <span data-ttu-id="86bee-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="86bee-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="86bee-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="86bee-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="86bee-106">La `SubpictureOn` proprietà imposta o recupera lo stato della sottoimmagine corrente (on o off).</span><span class="sxs-lookup"><span data-stu-id="86bee-106">The `SubpictureOn` property sets or retrieves the current subpicture state (on or off).</span></span>

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a><span data-ttu-id="86bee-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86bee-107">Return Value</span></span>

<span data-ttu-id="86bee-108">Restituisce un valore booleano che indica se viene visualizzata la sottoimmagine.</span><span class="sxs-lookup"><span data-stu-id="86bee-108">Returns a Boolean value indicating whether the subpicture is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="86bee-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="86bee-109">Remarks</span></span>

<span data-ttu-id="86bee-110">Questa proprietà non ha effetto sulla visualizzazione di didascalie chiuse.</span><span class="sxs-lookup"><span data-stu-id="86bee-110">This property does not affect display of Closed Captions.</span></span> <span data-ttu-id="86bee-111">I sottotitoli sono incorporati nel flusso video.</span><span class="sxs-lookup"><span data-stu-id="86bee-111">Closed Captions are embedded within the video stream.</span></span> <span data-ttu-id="86bee-112">Le sottoimmagini DVD vengono trasferite in un flusso separato.</span><span class="sxs-lookup"><span data-stu-id="86bee-112">DVD subpictures are transported on a separate stream.</span></span>

<span data-ttu-id="86bee-113">Quando il flusso di sottoimmagine viene modificato utilizzando [**CurrentSubpictureStream**](currentsubpicturestream-property.md), la `SubpictureOn` proprietà passa a **true**.</span><span class="sxs-lookup"><span data-stu-id="86bee-113">When the subpicture stream is changed using [**CurrentSubpictureStream**](currentsubpicturestream-property.md), the `SubpictureOn` property toggles to **True**.</span></span>

<span data-ttu-id="86bee-114">Questa proprietà è di lettura/scrittura e il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="86bee-114">This property is read/write with a default value of false.</span></span>

 

 



