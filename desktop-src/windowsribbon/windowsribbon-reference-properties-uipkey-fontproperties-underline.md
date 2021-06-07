---
title: UI_PKEY_FontProperties_Underline
description: Identifica la proprietà \_ FontProperties Underline dell'interfaccia \_ utente \_ PKEY.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443782"
---
# <a name="ui_pkey_fontproperties_underline"></a>UI \_ PKEY \_ FontProperties \_ Underline

Identifica la proprietà \_ FontProperties Underline dell'interfaccia \_ utente \_ PKEY.

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

Ui \_ PKEY \_ FontProperties \_ Underline viene usato da un'applicazione per eseguire query sullo stato del **pulsante Sottolineatura.**

Il valore della proprietà deriva [**dall'enumerazione \_ FONTUNDERLINE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) utente.

Il valore predefinito è `UI_FONTUNDERLINE_NOTSET`.

Lo screenshot seguente mostra il **pulsante Sottolinea** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-underline.png)

La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.



|      Proprietà                   |       Risultato dell'interfaccia utente                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | **Il pulsante** Sottolineatura è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTUNDERLINE_NOTSET`       | **Il pulsante** Sottolineatura non è selezionato.                                    |
| `UI_FONTUNDERLINE_SET`          | **Il pulsante** Sottolineatura è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTUNDERLINE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 