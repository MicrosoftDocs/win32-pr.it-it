---
title: Chiave di file_extension
description: Associa un'estensione di file a un ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856910"
---
# <a name="file_extension-key"></a><span data-ttu-id="10ccb-103">\_Chiave> estensione di file <</span><span class="sxs-lookup"><span data-stu-id="10ccb-103"><file\_extension> Key</span></span>

<span data-ttu-id="10ccb-104">Associa un'estensione di file a un ProgID.</span><span class="sxs-lookup"><span data-stu-id="10ccb-104">Associates a file name extension with a ProgID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="10ccb-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="10ccb-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a><span data-ttu-id="10ccb-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="10ccb-106">Remarks</span></span>

<span data-ttu-id="10ccb-107">Le informazioni contenute nella chiave di estensione del nome file vengono utilizzate sia da Esplora risorse che da moniker di file.</span><span class="sxs-lookup"><span data-stu-id="10ccb-107">The information contained in the file name extension key is used by both the Windows Explorer and file monikers.</span></span> <span data-ttu-id="10ccb-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa la chiave di estensione del nome file per fornire il CLSID associato.</span><span class="sxs-lookup"><span data-stu-id="10ccb-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) uses the file name extension key to supply the associated CLSID.</span></span>

<span data-ttu-id="10ccb-109">La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.</span><span class="sxs-lookup"><span data-stu-id="10ccb-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10ccb-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10ccb-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10ccb-111">**FileType**</span><span class="sxs-lookup"><span data-stu-id="10ccb-111">**FileType**</span></span>](filetype-key.md)
</dt> <dt>

[<span data-ttu-id="10ccb-112">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="10ccb-112">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




