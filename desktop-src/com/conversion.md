---
title: Conversione
description: Utilizzato dalla finestra di dialogo Converti per determinare i formati che un'applicazione può leggere e scrivere.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Chiave del Registro di sistema di conversione COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272090fb48b214daecd6350e6966350861366341fae055298a2fb2c90c9fb983
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993483"
---
# <a name="conversion"></a>Conversione

Utilizzato dalla finestra **di dialogo** Converti per determinare i formati che un'applicazione può leggere e scrivere.

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

Le informazioni di conversione vengono usate dalla **finestra di** dialogo Converti per determinare i formati che un'applicazione può leggere e scrivere. Un formato di file delimitato da virgole è indicato da un numero se è uno dei formati degli Appunti definiti in Windows.h. Una stringa indica che il formato non è definito in Windows.h (privato). In questo caso, il formato leggibile e scrivibile è CF \_ OUTLINE (private).

Il *valore rformat* specifica il formato di file che un'applicazione può leggere (convertire da).

Il *valore rwformat* specifica il formato di file che un'applicazione può leggere e scrivere (attiva come).

 

 




