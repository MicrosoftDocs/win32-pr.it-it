---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8d06c40fd88b525cadf9f90a1edd4edaaf3a9e9be7ccdcfa98dd6abf8b833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692644"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow::SetVisible

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Impostare la [**proprietà Visible**](visible-property.md) per la finestra Comandi vocali.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Impostazione della proprietà [**Visible.**](visible-property.md) Il valore **True visualizza** la finestra Comandi vocali. **False** lo nasconde.

</dd> </dl>

L'utente può eseguire l'override di questa proprietà.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandWindow::GetVisible**](iagentcommandwindow--getvisible.md)


 

 




