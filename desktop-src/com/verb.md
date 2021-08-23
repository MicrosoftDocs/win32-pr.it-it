---
title: Verbo
description: Specifica i verbi da registrare per un'applicazione.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Chiave del Registro di sistema verbo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef70e4a3f748b1f00a364f25755d60a3adfd9091cd2df3032e347f53f55519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047719"
---
# <a name="verb"></a>Verbo

Specifica i verbi da registrare per un'applicazione.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a>Commenti

Ogni verbo è un **valore REG \_ SZ** nel formato "*name*, *menu \_ flag*, *verb \_ flag*". I verbi devono essere numerati consecutivamente.

Il *nome* descrive il modo in cui il verbo viene aggiunto da una [**chiamata di funzione AppendMenu.**](/windows/win32/api/winuser/nf-winuser-appendmenua) Ad esempio, "&Play".

Il *valore \_ del flag* di menu indica la modalità di visualizzazione del verbo nel menu. Tutti i flag supportati [**da AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) sono supportati, ad eccezione di MF \_ BITMAP, MF \_ OWNERDRAW e MF \_ POPUP.

Il valore del flag del *\_ verbo* descrive gli attributi dei verbi. Usare uno dei valori di [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)o 0.

Per altre informazioni, vedere [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)e [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 