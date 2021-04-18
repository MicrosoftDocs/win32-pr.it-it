---
description: Il metodo StillOff riprende la riproduzione, annullando la modalità ancora.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Metodo StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314405"
---
# <a name="stilloff-method"></a><span data-ttu-id="bfae1-103">Metodo StillOff</span><span class="sxs-lookup"><span data-stu-id="bfae1-103">StillOff Method</span></span>

> [!Note]  
> <span data-ttu-id="bfae1-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bfae1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bfae1-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="bfae1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bfae1-106">Il `StillOff` Metodo riprende la riproduzione, annullando la modalità ancora.</span><span class="sxs-lookup"><span data-stu-id="bfae1-106">The `StillOff` method resumes playback, canceling still mode.</span></span>

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a><span data-ttu-id="bfae1-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfae1-107">Return Value</span></span>

<span data-ttu-id="bfae1-108">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bfae1-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfae1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfae1-109">Remarks</span></span>

<span data-ttu-id="bfae1-110">Il [navigatore DVD](dvd-navigator-filter.md) passa alla modalità ancora quando rileva un frame ancora creato sul disco. Invia una notifica all'applicazione inviando un \_ DVD EC \_ ancora \_ in un evento.</span><span class="sxs-lookup"><span data-stu-id="bfae1-110">The [DVD Navigator](dvd-navigator-filter.md) goes into still mode when it encounters a still frame authored on the disc. It notifies your application by sending an EC\_DVD\_STILL\_ON event.</span></span> <span data-ttu-id="bfae1-111">La modalità ancora è diversa da quella in cui lo strumento di spostamento DVD si trova in uno stato di sospensione a causa di un'operazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bfae1-111">Still mode is different from the DVD Navigator being in a paused state because of a user operation.</span></span> <span data-ttu-id="bfae1-112">`StillOff`La chiamata riprende la riproduzione dalla modalità ancora, ma non riavvia il navigatore DVD quando si trova in uno stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="bfae1-112">Calling `StillOff` resumes playback from still mode but does not restart the DVD Navigator when it is in a paused state.</span></span>

 

 



