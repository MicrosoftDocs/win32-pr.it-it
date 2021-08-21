---
title: UI_PKEY_Keytip
description: Identifica la proprietà \_ PKEY \_ Keytip dell'interfaccia utente.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940a855561dfd30dfbf063323f4b86b03561163c4fbf34f9db08be4eb3e1ece3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028609"
---
# <a name="ui_pkey_keytip"></a>Suggerimento \_ per la chiave PKEY \_ dell'interfaccia utente

Identifica la proprietà \_ PKEY \_ Keytip dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Commenti

La \_ descrizione comando PKEY \_ dell'interfaccia utente viene usata da un'applicazione per eseguire query sull'acceleratore di tastiera di un controllo barra multifunzione.

Il valore di questa proprietà è una stringa, composta da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti.

Il valore della descrizione comando PKEY dell'interfaccia utente funge da tasto di scelta rapida per un comando, a meno che tale comando non \_ venga esposto tramite una voce di \_ menu. In questo caso, il framework ignora il valore PKEY keytip dell'interfaccia utente e usa invece un carattere preceduto da una e commerciale come specificato da \_ \_ [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md). Se non viene specificata alcuna e commerciale da **Command.LabelTitle** o ui PKEY Label, non viene esposta alcuna descrizione comando o \_ tasto di scelta \_ rapida.

La lunghezza massima della descrizione comando \_ PKEY \_ dell'interfaccia utente non è associata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà risorsa](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.Keytip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




