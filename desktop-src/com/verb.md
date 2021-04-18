---
title: Verbo
description: Specifica i verbi da registrare per un'applicazione.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Chiave del registro di sistema verb COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300496"
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

Ogni verbo è un **valore \_ reg SZ** nel formato "*nome*, *\_ flag di menu*, *\_ flag verbo*". I verbi devono essere numerati consecutivamente.

Il *nome* descrive il modo in cui il verbo viene accodato da una chiamata di funzione [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) . Ad esempio, "&Play".

Il valore del *\_ flag di menu* indica il modo in cui il verbo dovrebbe essere visualizzato nel menu. Sono supportati tutti i flag supportati da [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , ad eccezione di MF \_ bitmap, MF \_ OWNERDRAW e MF \_ popup.

Il valore del *\_ flag verb* descrive gli attributi dei verbi. Usare uno dei valori di [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)o 0.

Per ulteriori informazioni, vedere [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)e [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 