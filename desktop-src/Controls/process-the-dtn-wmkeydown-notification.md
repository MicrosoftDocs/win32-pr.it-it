---
title: Come elaborare la notifica di DTN_WMKEYDOWN
description: In questo argomento viene illustrato come elaborare una \_ notifica di DTN WMKEYDOWN. La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873137"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Come elaborare la notifica DTN \_ WMKEYDOWN

In questo argomento viene illustrato come elaborare una notifica di [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


I controlli di selezione data e ora (DTP) inviano il messaggio [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) per segnalare che l'utente ha digitato l'input in un campo di callback. Se si desidera emulare le stesse risposte da tastiera supportate per i campi di DTP standard o fornire risposte personalizzate, l'applicazione deve includere il codice per gestire la notifica.

Il seguente esempio di codice C++ è una funzione definita dall'applicazione che elabora la notifica [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .

**Avviso di sicurezza:** L'uso errato di **lstrcmp** può compromettere la sicurezza dell'applicazione. Ad esempio, prima di chiamare **lstrcmp** nell'esempio di codice seguente, è necessario assicurarsi che le due stringhe abbiano terminazione null. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli selezione data e ora](using-date-and-time-picker.md)
</dt> <dt>

[Riferimento al controllo selezione data e ora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




