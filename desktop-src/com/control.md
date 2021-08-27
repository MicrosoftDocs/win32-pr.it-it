---
title: Control
description: Identifica un oggetto come controllo ActiveX controllo .
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Controllare la chiave del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa6a0b131dd5fc2ba10d9aaeabafd06b19b73bb1e9422c28e5bec45ea43cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120511"
---
# <a name="control"></a>Control

Identifica un oggetto come controllo ActiveX controllo .

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Commenti

Questa voce facoltativa viene usata dai contenitori per compilare le finestre di dialogo. Il contenitore usa questa sottochiave per determinare se includere un oggetto in una finestra di dialogo che visualizza ActiveX controlli. Un controllo può omettere questa voce se è progettato per funzionare solo con un contenitore specifico e pertanto non deve essere inserito in altri contenitori.

 

 




