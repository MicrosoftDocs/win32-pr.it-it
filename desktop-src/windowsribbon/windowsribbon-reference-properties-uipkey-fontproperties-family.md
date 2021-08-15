---
title: UI_PKEY_FontProperties_Family
description: Identifica la proprietà \_ della famiglia FontProperties PKEY \_ \_ dell'interfaccia utente.
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0574ea4fb104cff29b58c8b1f649bd9287672acef677e3ea4cdc6ad5f91367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438660"
---
# <a name="ui_pkey_fontproperties_family"></a>Famiglia \_ FontProperties PKEY \_ \_ dell'interfaccia utente

Identifica la proprietà \_ della famiglia FontProperties PKEY \_ \_ dell'interfaccia utente.

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

Ui \_ PKEY \_ FontProperties \_ Family viene usato da un'applicazione per eseguire query  sul valore della raccolta a discesa Della famiglia di caratteri.

Il valore di UI PKEY FontProperties Family corrisponde a un nome Windows GDI Font Families recuperato con la funzione \_ \_ \_ [EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) o [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa). [](../gdi/font-families.md)

Il valore predefinito è una stringa vuota.

Se viene specificata una stringa vuota per il valore per ui \_ PKEY \_ FontProperties Family, la selezione del tipo \_ di carattere viene cancellata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 