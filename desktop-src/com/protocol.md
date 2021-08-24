---
title: Protocollo
description: Indica che questa classe OLE 2 è inseribile nei contenitori OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Chiave del Registro di sistema del protocollo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7721e4f90a122fcbc519163d80c1e8e549f2b6aa05526d33d9693783abd1276a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130023"
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

La **voce StdFileEditing** specifica le informazioni di compatibilità OLE 1. Deve essere presente solo se gli oggetti di questa classe sono inseribili nei contenitori OLE 1.

**Server** specifica il percorso completo dell'applicazione server OLE 2 e **Verbo** specifica i verbi. Verbo 0 è il verbo primario e i verbi aggiuntivi devono essere numerati consecutivamente.

 

 




