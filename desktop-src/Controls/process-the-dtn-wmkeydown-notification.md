---
title: Come elaborare la DTN_WMKEYDOWN notifica
description: Questo argomento illustra come elaborare una notifica \_ WMKEYDOWN DTN. La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbef0804afb388f9cadad60b04bf93ce4730ef255476f0c7f216edfd24846a19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540351"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Come elaborare la notifica WMKEYDOWN DTN \_

Questo argomento illustra come elaborare una [notifica \_ WMKEYDOWN DTN.](dtn-wmkeydown.md) La gestione di questo codice di notifica consente al proprietario del controllo di fornire risposte specifiche alle sequenze di tasti all'interno dei campi di callback del controllo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


I controlli di selezione data e ora (DTP) inviano il messaggio [ \_ WMKEYDOWN DTN](dtn-wmkeydown.md) per segnalare che l'utente ha digitato l'input in un campo di callback. Se si desidera emulare le stesse risposte della tastiera supportate per i campi DTP standard o fornire risposte personalizzate, l'applicazione deve includere il codice per gestire questa notifica.

L'esempio di codice C++ seguente è una funzione definita dall'applicazione che elabora la notifica [ \_ WMKEYDOWN DTN.](dtn-wmkeydown.md)

**Avviso di sicurezza:** **L'uso non corretto di lstrcmp** può compromettere la sicurezza dell'applicazione. Ad esempio, prima di chiamare **lstrcmp** nell'esempio di codice seguente, è necessario assicurarsi che le due stringhe siano con terminazione Null. Prima di continuare, vedere Considerazioni sulla [sicurezza: Microsoft Windows Controlli.](sec-comctls.md)



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

[Uso dei controlli selezione data e ora](using-date-and-time-picker.md)
</dt> <dt>

[Informazioni di riferimento sul controllo Selezione data e ora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




