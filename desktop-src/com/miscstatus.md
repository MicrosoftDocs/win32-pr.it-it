---
title: MiscStatus
description: Specifica la modalità di creazione e visualizzazione di un oggetto.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044942"
---
# <a name="miscstatus"></a><span data-ttu-id="19b1d-104">MiscStatus</span><span class="sxs-lookup"><span data-stu-id="19b1d-104">MiscStatus</span></span>

<span data-ttu-id="19b1d-105">Specifica la modalità di creazione e visualizzazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="19b1d-105">Specifies how to create and display an object.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="19b1d-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="19b1d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a><span data-ttu-id="19b1d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="19b1d-107">Remarks</span></span>

<span data-ttu-id="19b1d-108">Per ulteriori informazioni, vedere l'enumerazione [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) e [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span><span class="sxs-lookup"><span data-stu-id="19b1d-108">For more information, see the [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) enumeration and [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span></span>

<span data-ttu-id="19b1d-109">Se non viene trovata alcuna sottochiave corrispondente a un DVASPECT, viene usato il valore predefinito di **miscStatus** .</span><span class="sxs-lookup"><span data-stu-id="19b1d-109">If no subkey that corresponds to a DVASPECT is found, the default value of **MiscStatus** is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19b1d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19b1d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b1d-111">**IOleObject:: GetMiscStatus**</span><span class="sxs-lookup"><span data-stu-id="19b1d-111">**IOleObject::GetMiscStatus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




