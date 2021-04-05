---
title: UI_PKEY_LabelDescription
description: Identifica la proprietà LabelDescription dell'interfaccia utente \_ pkey \_ .
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856414"
---
# <a name="ui_pkey_labeldescription"></a>Interfaccia utente \_ pkey \_ LabelDescription

Identifica la proprietà LabelDescription dell'interfaccia utente \_ pkey \_ .

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ LabelDescription viene usata da un'applicazione per eseguire una query sulla descrizione associata a un' [ \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md).

Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.

> [!Note]  
> Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.

 

La lunghezza massima è unbounded.

L'allineamento a destra non è supportato.

Lo screenshot seguente illustra l'uso di un'etichetta e di una descrizione dell'etichetta associata nel menu di un'applicazione.

![screenshot che mostra un'etichetta e una descrizione dell'etichetta associata nel menu di un'applicazione.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà delle risorse](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




