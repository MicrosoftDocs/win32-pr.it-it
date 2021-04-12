---
title: Control
description: Identifica un oggetto come controllo ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Controllare la chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396866"
---
# <a name="control"></a>Control

Identifica un oggetto come controllo ActiveX.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Commenti

Questa voce facoltativa viene usata dai contenitori per compilare le finestre di dialogo. Il contenitore utilizza questa sottochiave per determinare se includere un oggetto in una finestra di dialogo in cui sono visualizzati i controlli ActiveX. Un controllo può omettere questa voce se è progettata per funzionare solo con un contenitore specifico e pertanto non è destinata all'inserimento in altri contenitori.

 

 




