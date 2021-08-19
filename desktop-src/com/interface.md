---
title: Interfaccia (COM)
description: Voce facoltativa che specifica tutti gli ID di interfaccia (IID) supportati dalla classe associata.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Chiave del Registro di sistema dell'interfaccia COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d8eaa38b97896f623c8d9f245c48f8d12634f930dc193cba14d5a9217a261e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048119"
---
# <a name="interface-com"></a>Interfaccia (COM)

Voce facoltativa che specifica tutti gli ID di interfaccia (IID) supportati dalla classe associata.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>Commenti

Se un nome di interfaccia non è presente in questo elenco, l'interfaccia non può mai essere supportata da un'istanza di questa classe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiave interfaccia](interface-key.md)
</dt> </dl>

 

 




