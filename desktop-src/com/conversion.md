---
title: Conversione
description: Utilizzato dalla finestra di dialogo Converti per determinare i formati che possono essere letti e scritti da un'applicazione.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Conversione della chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516072"
---
# <a name="conversion"></a>Conversione

Utilizzato dalla finestra di dialogo **Converti** per determinare i formati che possono essere letti e scritti da un'applicazione.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a>Commenti

Le informazioni sulla conversione vengono utilizzate dalla finestra di dialogo **Converti** per determinare i formati che possono essere letti e scritti da un'applicazione. Un formato di file delimitato da virgole è indicato da un numero se è uno dei formati degli Appunti definiti in Windows. h. Una stringa indica che il formato non è definito in Windows. h (privato). In questo caso, il formato leggibile e scrivibile è la \_ struttura CF (privata).

Il valore *rformat* specifica il formato di file che un'applicazione può leggere (da cui eseguire la conversione).

Il valore *rwformat* specifica il formato di file che un'applicazione può leggere e scrivere (attivare come).

 

 




