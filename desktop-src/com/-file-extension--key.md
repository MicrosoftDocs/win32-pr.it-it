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
# <a name="file_extension-key"></a>\_Chiave> estensione di file <

Associa un'estensione di file a un ProgID.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Commenti

Le informazioni contenute nella chiave di estensione del nome file vengono utilizzate sia da Esplora risorse che da moniker di file. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa la chiave di estensione del nome file per fornire il CLSID associato.

La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**FileType**](filetype-key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




