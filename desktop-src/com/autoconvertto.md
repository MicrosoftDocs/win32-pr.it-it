---
title: AutoConvertTo
description: Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- AutoConvertTo chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855185"
---
# <a name="autoconvertto"></a><span data-ttu-id="65cc7-104">AutoConvertTo</span><span class="sxs-lookup"><span data-stu-id="65cc7-104">AutoConvertTo</span></span>

<span data-ttu-id="65cc7-105">Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="65cc7-105">Specifies the automatic conversion of a given class of objects to a new class of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="65cc7-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="65cc7-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a><span data-ttu-id="65cc7-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="65cc7-107">Remarks</span></span>

<span data-ttu-id="65cc7-108">Si tratta di un valore **reg \_ SZ** che specifica l'identificatore di classe dell'oggetto in cui deve essere convertito l'oggetto o la classe di oggetti specificata.</span><span class="sxs-lookup"><span data-stu-id="65cc7-108">This is a **REG\_SZ** value that specifies the class identifier of the object to which the given object or class of objects should be converted.</span></span>

<span data-ttu-id="65cc7-109">Questa chiave viene in genere utilizzata per convertire automaticamente i file creati da una versione precedente di un'applicazione in una versione più recente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="65cc7-109">This key is typically used to automatically convert files created by an older version of an application to a newer version of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65cc7-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65cc7-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65cc7-111">**OleDoAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="65cc7-111">**OleDoAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[<span data-ttu-id="65cc7-112">**OleGetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="65cc7-112">**OleGetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[<span data-ttu-id="65cc7-113">**OleSetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="65cc7-113">**OleSetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




