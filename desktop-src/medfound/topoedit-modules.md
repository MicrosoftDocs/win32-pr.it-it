---
description: Moduli TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Moduli TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049799"
---
# <a name="topoedit-modules"></a>Moduli TopoEdit

Lo strumento TopoEdit viene fornito con la Windows SDK per Windows Server 2008 e versioni successive. Lo strumento richiede Windows Vista o versione successiva.

I moduli TopoEdit si trovano nella cartella bin dell'SDK. Questi moduli sono:

-   TopoEdit.exe: eseguibile dell'applicazione
-   TEDUTIL.dll-DLL di estensione

L'installazione dell'SDK registra la DLL. Tuttavia, in caso di errore, al prompt dei comandi eseguire il comando seguente.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



Il codice sorgente per TopoEdit viene fornito anche come esempio nell'Windows SDK. Si trova nella directory seguente:

<samples root>\\Multimedia \\ Media Foundation \\ TopoEdit

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione a TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



