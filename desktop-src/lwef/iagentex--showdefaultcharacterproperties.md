---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362cffa8d4b34d70111505a60fd5eadc68a220cd45c3beb519e5e39ba62f1a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749815"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Visualizza la finestra delle proprietà dei caratteri predefinita.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata x della finestra in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata y della finestra in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

Flag di posizione predefinito. Se questo parametro è **True**, Microsoft Agent visualizza la finestra della finestra delle proprietà per il carattere predefinito nell'ultima posizione in cui è stato visualizzato.

> [!Note]  
> Per Windows 2000, potrebbe essere necessario chiamare la nuova API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) per assicurarsi che questa finestra diventi la finestra in primo piano. Per altre informazioni sull'impostazione della finestra in primo piano Windows 2000, vedere la documentazione di Platform SDK.

 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 