---
title: UI_PKEY_Pinned
description: Identifica la proprietà bloccata dell'interfaccia utente \_ pkey \_ .
ms.assetid: 906b2ab9-1ed7-46a6-88bc-e8f9160ab60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8637f11404090313751647058ee41acbad3d9bf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221738"
---
# <a name="ui_pkey_pinned"></a>Interfaccia utente \_ pkey \_ bloccata

Identifica la proprietà bloccata dell'interfaccia utente \_ pkey \_ .

```
propertyDescription
   name = UI_PKEY_Pinned
   shellPKey = UI_PKEY_Pinned
   formatID = 00000351-7363-696e-8441798acf5aebb7
   propID = 351
   typeInfo
      type = VT_BOOL
   booleanFormat
      formatAs = VARIANT_TRUE=-1, VARIANT_FALSE=0
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey aggiunta \_ viene usata da un'applicazione per eseguire una query per verificare se un elemento nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) è "bloccato" o persistente tra le istanze dell'applicazione. Ad esempio, un elemento nell'elenco degli elementi usati di recente (MRU) è accessibile e non rilascia l'elenco di elementi MRU finché non è "sbloccato".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà stato](windowsribbon-reference-properties-state.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md)
</dt> <dt>

[Elementi recenti](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 




