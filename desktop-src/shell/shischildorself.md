---
UID: ''
title: SHIsChildOrSelf (funzione)
description: Consente di confrontare se una finestra è uguale a, figlio di o discendente di una seconda finestra.
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
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104993304"
---
# <a name="shischildorself-function"></a>SHIsChildOrSelf (funzione)

## <a name="description"></a>Descrizione

\[Questa funzione è disponibile tramite Windows XP e Windows Server 2003.
Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Consente di confrontare se una finestra è uguale a, figlio di o discendente di una seconda finestra.

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

### <a name="hwnd-in"></a>HWND [in]

Tipo: **HWND**

Handle per una finestra da testare rispetto a *hwndParent*.

## <a name="returns"></a>Restituisce

Tipo: **HRESULT**

Restituisce **S_OK** se la finestra specificata da *HWND* è uguale a, un elemento figlio di o un discendente della finestra specificata da *hwndParent*.
Restituisce **S_FALSE** se la finestra specificata da HWND non è uguale a, non è un elemento figlio di e non è un discendente della finestra specificata da *hwndParent*.
Il valore restituito non è definito se uno degli handle della finestra non è valido.

## <a name="remarks"></a>Commenti

## <a name="see-also"></a>Vedi anche

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
