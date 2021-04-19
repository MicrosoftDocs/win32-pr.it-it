---
description: La proprietà SubpictureStreamsAvailable Recupera il numero di flussi di immagini subimmagine disponibili nel titolo corrente.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Proprietà SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317835"
---
# <a name="subpicturestreamsavailable-property"></a><span data-ttu-id="67c96-103">Proprietà SubpictureStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="67c96-103">SubpictureStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="67c96-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="67c96-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="67c96-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="67c96-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="67c96-106">La `SubpictureStreamsAvailable` proprietà recupera il numero di flussi di immagini subimmagine disponibili nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="67c96-106">The `SubpictureStreamsAvailable` property retrieves the number of subpicture streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="67c96-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67c96-107">Return Value</span></span>

<span data-ttu-id="67c96-108">Restituisce il numero di flussi disponibili come Integer.</span><span class="sxs-lookup"><span data-stu-id="67c96-108">Returns the number of available streams as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c96-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="67c96-109">Remarks</span></span>

<span data-ttu-id="67c96-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="67c96-110">This property is read-only with no default value.</span></span> <span data-ttu-id="67c96-111">Per eseguire una query su ogni flusso per il relativo attributo Language, chiamare innanzitutto questo metodo per ottenere il limite superiore.</span><span class="sxs-lookup"><span data-stu-id="67c96-111">To query each stream for its language attribute, first call this method to get the upper bound.</span></span>

<span data-ttu-id="67c96-112">La numerazione del flusso è in base zero.</span><span class="sxs-lookup"><span data-stu-id="67c96-112">Stream numbering is zero-based.</span></span>

 

 



