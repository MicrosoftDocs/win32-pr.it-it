---
title: Interfaccia (COM)
description: Voce facoltativa che specifica tutti gli ID di interfaccia (IID) supportati dalla classe associata.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Chiave del registro di sistema Interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300881"
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

Se un nome di interfaccia non è presente nell'elenco, l'interfaccia non può mai essere supportata da un'istanza di questa classe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiave interfaccia](interface-key.md)
</dt> </dl>

 

 




