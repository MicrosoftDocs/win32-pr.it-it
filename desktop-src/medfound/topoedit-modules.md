---
description: Moduli TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Moduli TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc95848a533ba67599c114917ebe502f42a4fe859df9c1ac6bf5acfc40bb393c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057716"
---
# <a name="topoedit-modules"></a>Moduli TopoEdit

Lo strumento TopoEdit viene fornito con Windows SDK per Windows Server 2008 e versioni successive. Lo strumento richiede Windows Vista o versione successiva.

I moduli TopoEdit si trovano nella cartella Bin dell'SDK. Questi moduli sono:

-   TopoEdit.exe: eseguibile dell'applicazione
-   TEDUTIL.dll: DLL di estensione

L'installazione dell'SDK registra la DLL. Se tuttavia l'operazione non riesce, al prompt dei comandi eseguire quanto segue.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



Il codice sorgente per TopoEdit viene fornito anche come esempio in Windows SDK. Si trova nella directory seguente:

<samples root>\\Elementi \\ Media Foundation \\ TopoModifica

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione a TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopoModifica](topoedit.md)
</dt> </dl>

 

 



