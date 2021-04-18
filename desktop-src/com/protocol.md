---
title: Protocollo
description: Indica che questa classe OLE 2 è inseribile nei contenitori OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Chiave del registro di sistema protocollo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298611"
---
# <a name="protocol"></a>Protocollo

Indica che questa classe OLE 2 è inseribile nei contenitori OLE 1.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a>Commenti

La voce **StdFileEditing** specifica le informazioni sulla compatibilità OLE 1. Deve essere presente solo se gli oggetti di questa classe possono essere inseriti in contenitori OLE 1.

**Server** specifica il percorso completo dell'applicazione server OLE 2 e il **verbo** specifica i verbi. Il verbo 0 è il verbo principale e i verbi aggiuntivi devono essere numerati consecutivamente.

 

 




