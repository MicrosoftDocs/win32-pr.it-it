---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la \_ \_ proprietà barrata pkey FontProperties dell'interfaccia utente \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399561"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>Barra dell'interfaccia utente \_ pkey \_ FontProperties \_

Identifica la \_ \_ proprietà barrata pkey FontProperties dell'interfaccia utente \_ .

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

UI \_ pkey \_ FontProperties \_ barrato viene usato da un'applicazione per eseguire una query sullo stato del pulsante **barrato** .

Il valore della proprietà è dall' [**enumerazione \_ FONTPROPERTIES dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.

Lo screenshot seguente mostra il pulsante **barrato** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-strikethrough.png)

Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Il pulsante **barrato** è disabilitato e può essere impostato solo dall'applicazione. |
| `UI_FONTPROPERTIES_NOTSET`       | Il pulsante **barrato** non è selezionato.                                    |
| `UI_FONTPROPERTIES_SET`          | Il pulsante **barrato** è selezionato.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 