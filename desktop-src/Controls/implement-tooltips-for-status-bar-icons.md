---
title: Come implementare le descrizioni comandi per le icone della barra di stato
description: Un modo non intrusivo per visualizzare un messaggio esplicativo per un'icona della barra di stato consiste nell'implementare una descrizione comando. La descrizione comando scompare quando si fa clic, ma è anche possibile specificare un valore di timeout.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474398"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Come implementare le descrizioni comandi per le icone della barra di stato

Un modo non intrusivo per visualizzare un messaggio esplicativo per un'icona della barra di stato consiste nell'implementare una descrizione comando. La descrizione comando scompare quando si fa clic, ma è anche possibile specificare un valore di timeout.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="implement-tooltips-for-status-bar-icons"></a>Implementa descrizioni comandi per le icone della barra di stato

Il frammento di codice seguente illustra come aggiungere una descrizione comando Balloon a un'icona della barra di stato.


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a>Commenti

Per una descrizione dettagliata della barra di stato, vedere [la barra delle applicazioni](/windows/desktop/shell/taskbar).

Per visualizzare una descrizione comando a fumetti, è necessario impostare il \_ flag NSE info nella struttura [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) e usare i membri **szInfo** e **uTimeout** per specificare il testo della descrizione comando e la durata del timeout.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 