---
description: La proprietà ColorKey imposta o recupera la chiave di colore utilizzata per la didascalia chiusa.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Proprietà ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481180"
---
# <a name="colorkey-property"></a><span data-ttu-id="1564c-103">Proprietà ColorKey</span><span class="sxs-lookup"><span data-stu-id="1564c-103">ColorKey Property</span></span>

> [!Note]  
> <span data-ttu-id="1564c-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1564c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1564c-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="1564c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1564c-106">La `ColorKey` proprietà imposta o recupera la chiave di colore utilizzata per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="1564c-106">The `ColorKey` property sets or retrieves the color key used in closed captioning.</span></span>

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a><span data-ttu-id="1564c-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1564c-107">Return Value</span></span>

<span data-ttu-id="1564c-108">Restituisce un valore intero che rappresenta il colore da utilizzare come sfondo trasparente per il testo con didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="1564c-108">Returns an integer value representing the color to use as a transparent background for closed-captioned text.</span></span> <span data-ttu-id="1564c-109">Il valore predefinito in colori 256 è magenta e nero in qualsiasi altra profondità di colore.</span><span class="sxs-lookup"><span data-stu-id="1564c-109">The default value in 256 colors is magenta, and off-black in any other color depth.</span></span>

## <a name="remarks"></a><span data-ttu-id="1564c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1564c-110">Remarks</span></span>

<span data-ttu-id="1564c-111">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1564c-111">This property is read/write.</span></span> <span data-ttu-id="1564c-112">Questa proprietà si applica solo alle didascalie chiuse, se presenti, non al flusso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1564c-112">This property applies only to the closed-captions, if any exist, not to the subpicture stream.</span></span>

 

 



