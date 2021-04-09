---
title: UI_PKEY_Keytip
description: Identifica la proprietà del suggerimento dell'interfaccia utente \_ pkey \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955537"
---
# <a name="ui_pkey_keytip"></a>Suggerimento tasto di interfaccia utente \_ pkey \_

Identifica la proprietà del suggerimento dell'interfaccia utente \_ pkey \_ .

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

L'interfaccia utente \_ \_ del suggerimento utente pkey viene utilizzata da un'applicazione per eseguire una query sull'acceleratore tastiera di un controllo Ribbon.

Il valore di questa proprietà è una stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti.

Il valore del \_ tasto di \_ scelta rapida UI pkey funge da tasto di scelta rapida per un comando, a meno che il comando non venga esposto tramite una voce di menu. In questo caso, il Framework ignora il valore del \_ suggerimento tasto di pkey dell'interfaccia utente \_ e usa invece un carattere preceduto da una e commerciale come specificato dall'etichetta [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md). Se nessuna e commerciale è specificata da **Command. LabelTitle** o dall'etichetta pkey dell'interfaccia utente \_ \_ , non viene esposto alcun tasto di scelta rapida o tasto di scelta rapida.

La lunghezza massima del suggerimento tasto di pkey dell'interfaccia utente \_ \_ è unbounded.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà delle risorse](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. suggerimento**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




