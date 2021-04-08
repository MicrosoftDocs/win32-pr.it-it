---
title: MiscStatus
description: Specifica la modalità di creazione e visualizzazione di un oggetto.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044942"
---
# <a name="miscstatus"></a>MiscStatus

Specifica la modalità di creazione e visualizzazione di un oggetto.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Commenti

Per ulteriori informazioni, vedere l'enumerazione [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) e [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Se non viene trovata alcuna sottochiave corrispondente a un DVASPECT, viene usato il valore predefinito di **miscStatus** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




