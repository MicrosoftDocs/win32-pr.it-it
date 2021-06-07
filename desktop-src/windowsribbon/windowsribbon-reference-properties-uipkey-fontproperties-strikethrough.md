---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la proprietà \_ PKEY \_ FontProperties \_ Strikethrough dell'interfaccia utente.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443792"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>Carattere \_ PKEY \_ dell'interfaccia \_ utenteProprietà barrato

Identifica la proprietà \_ PKEY \_ FontProperties \_ Strikethrough dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Commenti

Ui \_ PKEY \_ FontProperties \_ Strikethrough viene usato da un'applicazione per eseguire query sullo stato del **pulsante Barrato.**

Il valore della proprietà deriva [**dall'enumerazione \_ FONTPROPERTIES dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) utente.

Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.

Lo screenshot seguente mostra il **pulsante Barrato** della barra [**multifunzione FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-strikethrough.png)

La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.



|   Proprietà                       |    Risultato dell'interfaccia utente                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Il pulsante barrato** è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTPROPERTIES_NOTSET`       | **Il pulsante Barrato** non è selezionato.                                    |
| `UI_FONTPROPERTIES_SET`          | **Il pulsante Barrato** è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**PROPRIETÀ FONT \_ DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 