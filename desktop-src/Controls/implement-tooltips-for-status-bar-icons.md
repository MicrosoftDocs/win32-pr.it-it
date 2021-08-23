---
title: Come implementare le descrizioni comando per le icone della barra di stato
description: Un modo non intrusivo per visualizzare un messaggio esplicativo per un'icona della barra di stato è implementare una descrizione comando. La descrizione comando scompare quando si fa clic, ma è anche possibile specificare un valore di timeout.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bd100dc6edb2aac7b4c8c5df3781e76391ae2d9d0ad456533384ed8701f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958580"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Come implementare le descrizioni comando per le icone della barra di stato

Un modo non intrusivo per visualizzare un messaggio esplicativo per un'icona della barra di stato è implementare una descrizione comando. La descrizione comando scompare quando si fa clic, ma è anche possibile specificare un valore di timeout.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="implement-tooltips-for-status-bar-icons"></a>Implementare descrizioni comando per le icone della barra di stato

Il frammento di codice seguente illustra come aggiungere una descrizione comando a forma di fumetto a un'icona della barra di stato.


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

Per una descrizione dettagliata della barra di stato, vedere Barra [delle applicazioni.](/windows/desktop/shell/taskbar)

Per visualizzare una descrizione comando a fumetto, è necessario impostare il flag NIF INFO nella struttura NOTIFYICONDATA e usare i membri \_ **szInfo** e **uTimeout** per specificare il testo della descrizione comando e la durata del timeout. [](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli descrizione comando](using-tooltip-contro.md)
</dt> </dl>

 

 