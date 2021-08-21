---
title: UI_PKEY_LabelDescription
description: Identifica la proprietà \_ Ui PKEY \_ LabelDescription.
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80a2db487988f66fcc393b3ba449dfda789248dabc3cd9e1d3e48acf9ba3473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437999"
---
# <a name="ui_pkey_labeldescription"></a>UI \_ PKEY \_ LabelDescription

Identifica la proprietà \_ Ui PKEY \_ LabelDescription.

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

UI \_ PKEY \_ LabelDescription viene usato da un'applicazione per eseguire query sulla descrizione associata a [un'etichetta \_ PKEY dell'interfaccia \_ utente.](windowsribbon-reference-properties-uipkey-label.md)

Il valore della proprietà è una stringa vincolata a qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.

> [!Note]  
> Usare il riferimento ai caratteri XML del set di caratteri universali (UCS) `&#xA;` per specificare un'interruzione di riga.

 

La lunghezza massima è illimitata.

L'allineamento a destra non è supportato.

La schermata seguente illustra l'uso di un'etichetta e di una descrizione dell'etichetta associata in un menu dell'applicazione.

![Screenshot che mostra un'etichetta e una descrizione dell'etichetta associata in un menu dell'applicazione.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà risorsa](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[Etichetta \_ PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




