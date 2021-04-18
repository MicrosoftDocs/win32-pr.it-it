---
title: UI_PKEY_FontProperties_Family
description: Identifica la \_ proprietà della \_ famiglia FontProperties pkey dell'interfaccia utente \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299883"
---
# <a name="ui_pkey_fontproperties_family"></a>Interfaccia \_ utente \_ pkey \_ famiglia FontProperties

Identifica la \_ proprietà della \_ famiglia FontProperties pkey dell'interfaccia utente \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Commenti

Interfaccia utente \_ pkey \_ FontProperties la \_ famiglia viene utilizzata da un'applicazione per eseguire una query sul valore della raccolta a discesa della **famiglia di caratteri** .

Il valore della \_ famiglia pkey FontProperties di interfaccia utente \_ \_ corrisponde a un nome di [famiglie di caratteri GDI Windows](../gdi/font-families.md) recuperato con la [funzione EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) o [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).

Il valore predefinito è una stringa vuota.

Se viene fornita una stringa vuota per il valore per l'interfaccia utente \_ pkey \_ FontProperties \_ Family, la selezione del tipo di carattere viene deselezionata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 