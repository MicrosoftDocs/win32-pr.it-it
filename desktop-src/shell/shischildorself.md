---
UID: ''
title: Funzione SHIsChildOrSelf
description: Confronta se una finestra è uguale a, un elemento figlio di o un discendente di una seconda finestra.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: f2d8eaab0f17647a6f548a0243199073baef074c88dad6a3f7100cfbca1a02be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941331"
---
# <a name="shischildorself-function"></a>Funzione SHIsChildOrSelf

## <a name="description"></a>Descrizione

\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003.
Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Confronta se una finestra è uguale a, un elemento figlio di o un discendente di una seconda finestra.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Parametri

### <a name="hwndparent-in"></a>hwndParent [in]

Tipo: **HWND**

Handle per la prima finestra.

### <a name="hwnd-in"></a>hwnd [in]

Tipo: **HWND**

Handle per una finestra da testare con *hwndParent.*

## <a name="returns"></a>Restituisce

Tipo: **HRESULT**

Restituisce **S_OK** se la finestra specificata da *hwnd* è uguale a, un figlio di o un discendente della finestra specificata da *hwndParent.*
Restituisce **S_FALSE** se la finestra specificata da hwnd non è uguale a, non è figlio di e non è un discendente della finestra specificata da *hwndParent.*
Il valore restituito non è definito se uno degli handle di finestra non è valido.

## <a name="remarks"></a>Commenti

## <a name="see-also"></a>Vedi anche

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
