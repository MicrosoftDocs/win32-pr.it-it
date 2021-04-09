---
title: ToolBoxBitmap32
description: Identifica il nome del modulo e l'ID di risorsa per una bitmap 16 x 16 da usare per la superficie di una barra degli strumenti o un pulsante della casella degli strumenti.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- ToolBoxBitmap32 chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044536"
---
# <a name="toolboxbitmap32"></a>ToolBoxBitmap32

Identifica il nome del modulo e l'ID di risorsa per una bitmap 16 x 16 da usare per la superficie di una barra degli strumenti o un pulsante della casella degli strumenti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica il nome del modulo e l'identificatore di risorsa per la bitmap.

Le dimensioni dell'icona standard di Windows sono troppo grandi per essere usate a questo scopo. Questa operazione richiede contenitori di controllo con una modalità di progettazione in cui uno seleziona i controlli e li inserisce in un modulo progettato.

 

 




