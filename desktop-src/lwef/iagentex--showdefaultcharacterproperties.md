---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473059"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Visualizza la finestra Proprietà carattere predefinito.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata x della finestra, in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata y della finestra, in pixel, rispetto all'origine della schermata (in alto a sinistra).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

Flag di posizione predefinito. Se questo parametro è **true**, Microsoft Agent Visualizza la finestra delle proprietà per il carattere predefinito nell'ultima posizione in cui è comparso.

> [!Note]  
> Per Windows 2000, potrebbe essere necessario chiamare la nuova API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) per assicurarsi che questa finestra diventi la finestra in primo piano. Per ulteriori informazioni sull'impostazione della finestra in primo piano in Windows 2000, vedere la documentazione di Platform SDK.

 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 