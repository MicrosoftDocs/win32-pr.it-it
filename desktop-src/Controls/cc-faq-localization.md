---
title: Supporto della localizzazione per i controlli comuni
description: In questo argomento viene descritto il supporto per le lingue nazionali integrate nei controlli comuni.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955263"
---
# <a name="localization-support-for-common-controls"></a>Supporto della localizzazione per i controlli comuni

In questo argomento viene descritto il supporto per le lingue nazionali integrate nei controlli comuni. Il supporto del linguaggio nazionale integrato semplifica l'implementazione delle applicazioni localizzate.

In questo argomento sono incluse le sezioni seguenti:

-   [Specifica di una lingua per i controlli comuni](#specifying-a-language-for-the-common-controls)
-   [Specifica di una lingua per i controlli in una finestra di dialogo](#specifying-a-language-for-controls-in-a-dialog-box)
-   [Argomenti correlati](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a>Specifica di una lingua per i controlli comuni

Se si desidera specificare una lingua per i controlli comuni diversi dalla lingua di sistema, chiamare [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). La lingua specificata da questa funzione si applica solo al processo da cui viene chiamata la funzione.

Per determinare la lingua attualmente utilizzata dai controlli comuni, chiamare [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage). Restituisce il valore impostato da una chiamata precedente a [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). Il linguaggio restituito è quello specificato per il processo da cui viene chiamato. Se **InitMUILanguage** non è stato chiamato o è stato chiamato da un altro processo, **GetMUILanguage** restituirà un valore predefinito.

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a>Specifica di una lingua per i controlli in una finestra di dialogo

A differenza dei controlli comuni, i controlli predefiniti, quali pulsanti o caselle di modifica, non usano la lingua di sistema corrente per impostazione predefinita. Il controllo del tipo di carattere nativo è un controllo invisibile che funziona in background per consentire ai controlli predefiniti di una finestra di dialogo di visualizzare la lingua del sistema corrente.

Per usare il controllo del tipo di carattere nativo, seguire questa procedura.

1.  Inizializzare il controllo del tipo di carattere nativo chiamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Impostare il membro **dwICC** della struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) a cui punta *lpInitCtrls* alla classe ICC \_ NATIVEFNTCTL \_ .
2.  Aggiungere il controllo allo script di risorsa per la finestra di dialogo. Impostare uno o più dei flag di stile seguenti per specificare quali controlli saranno interessati. 

    | Contrassegno              | Si applica a                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_modifica NFS         | Controlli di modifica                                                                                                                                                                                                                                                    |
    | NFS \_ statico       | Controlli statici                                                                                                                                                                                                                                                  |
    | \_LISTCOMBO NFS    | Controlli List, ComboBox, List-View e ComboBoxEx                                                                                                                                                                                                               |
    | \_pulsante NFS       | Controlli pulsante                                                                                                                                                                                                                                                  |
    | NFS \_ tutto          | Tutti i controlli                                                                                                                                                                                                                                                     |
    | \_USEFONTASSOC NFS | Piattaforma Asia orientale. Il controllo Usa la funzionalità di associazione dei tipi di carattere anziché passare al tipo di carattere nativo. Tutte le altre piattaforme lo ignorano. Questa funzionalità è deprecata per Windows Vista e non è supportata in COMCTL V6. Questo esiste in COMCTL V5 per motivi di compatibilità con le versioni precedenti. |

    

     

Nell'esempio seguente viene illustrato come aggiungere un controllo del tipo di carattere nativo a uno script di risorsa. La finestra di dialogo modifica, elenco e casella combinata consente di visualizzare il testo utilizzando la lingua del sistema corrente.


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli comuni](common-controls-intro.md)
</dt> </dl>

 

 




