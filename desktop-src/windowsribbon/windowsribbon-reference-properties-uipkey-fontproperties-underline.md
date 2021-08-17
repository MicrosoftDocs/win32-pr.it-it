---
title: UI_PKEY_FontProperties_Underline
description: Identifica la proprietà \_ FontProperties Underline PKEY \_ \_ dell'interfaccia utente.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75142e08549c2084ebcd37e82943ed63fdfb5b278faef01c4ad79441fa36915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706722"
---
# <a name="ui_pkey_fontproperties_underline"></a>UI \_ PKEY \_ FontProperties \_ Underline

Identifica la proprietà \_ FontProperties Underline PKEY \_ \_ dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Commenti

UI \_ PKEY \_ FontProperties \_ Underline viene usato da un'applicazione per eseguire una query sullo stato del **pulsante Sottolineato.**

Il valore della proprietà deriva [**dall'enumerazione \_ FONTUNDERLINE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) utente.

Il valore predefinito è `UI_FONTUNDERLINE_NOTSET`.

Lo screenshot seguente mostra il pulsante **Sottolineato** del controllo [**FontControl della barra multifunzione.**](windowsribbon-element-fontcontrol.md)

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-underline.png)

La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.



|      Proprietà                   |       Risultato dell'interfaccia utente                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | **Il** pulsante Sottolineatura è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTUNDERLINE_NOTSET`       | **Il pulsante** Sottolineatura non è selezionato.                                    |
| `UI_FONTUNDERLINE_SET`          | **Il pulsante** Sottolineatura è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**CARATTERE \_ DELL'INTERFACCIA UTENTEUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Controllo Font](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 