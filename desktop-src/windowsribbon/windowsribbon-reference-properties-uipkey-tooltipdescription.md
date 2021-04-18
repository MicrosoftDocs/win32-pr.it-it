---
title: UI_PKEY_TooltipDescription
description: Identifica la proprietà TooltipDescription dell'interfaccia utente \_ pkey \_ .
ms.assetid: 658e798a-f41e-4538-94ac-38a9cb20dd74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900610c1302d3cc904dcde2d7c86801982fd4d10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298933"
---
# <a name="ui_pkey_tooltipdescription"></a>Interfaccia utente \_ pkey \_ TooltipDescription

Identifica la proprietà TooltipDescription dell'interfaccia utente \_ pkey \_ .

```
propertyDescription
   name = UI_PKEY_TooltipDescription
   shellPKey = UI_PKEY_TooltipDescription
   formatID = 00000005-7363-696e-8441798acf5aebb7
   propID = 5
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ TooltipDescription viene usata da un'applicazione per eseguire una query sulla descrizione associata a un' [interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md).

Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.

> [!Note]  
> Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.

 

La lunghezza massima dell'interfaccia utente \_ pkey \_ TooltipDescription è unbounded.

L'allineamento a destra non è supportato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà delle risorse](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)
</dt> <dt>

[Interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 




