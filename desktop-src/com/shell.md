---
title: Shell (COM)
description: Fornisce informazioni sulla stampa della shell di Windows 3,1 e sui file aperti.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Chiave del registro di sistema shell COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739346"
---
# <a name="shell-com"></a>Shell (COM)

Fornisce informazioni sulla stampa della shell di Windows 3,1 e sui **file aperti** .

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a>Commenti

Queste voci devono fornire il percorso e il nome file dell'applicazione.

 

 




