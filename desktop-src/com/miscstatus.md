---
title: MiscStatus
description: Specifica come creare e visualizzare un oggetto .
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Chiave del Registro di sistema MiscStatus COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41aa5a5ab7f777eb6aa19d919c69ca219c9364cd1d6e5e9471cb677300d4ebb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992351"
---
# <a name="miscstatus"></a>MiscStatus

Specifica come creare e visualizzare un oggetto .

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Commenti

Per altre informazioni, vedere [**l'enumerazione OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) e [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Se non viene trovata alcuna sottochiave corrispondente a DVASPECT, viene usato il valore predefinito **MiscStatus.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




