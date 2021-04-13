---
title: Uso dell'annotazione della mappa di valori
description: Per il codice di esempio, vedere esempio di annotazione della mappa dei valori.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399080"
---
# <a name="using-value-map-annotation"></a>Uso dell'annotazione della mappa di valori

**Per creare una mappa di valori**

1.  **Creare una stringa di mapping.**

    Una stringa di mapping è un elenco di valori numerici di un controllo corrispondenti a una stringa leggibile in Unicode. Inizia con "A:" seguito da un numero che indica il tipo di indice usato. Sono supportati solo gli indici di immagini; Pertanto, il tipo di indice è sempre 0.

    La stringa è seguita da coppie index: result. "Index" è un numero che rappresenta un indice di immagine per un List-View o una visualizzazione ad albero oppure il valore per un controllo dispositivo di scorrimento.

    Il valore risultante è un numero ottenuto quando si esegue il mapping della proprietà Role o state per una visualizzazione elenco o un controllo di visualizzazione ad albero. Tali numeri sono espressi in formato decimale o esadecimale con prefisso "0x".

    La stringa di mapping viene sempre terminata con i due punti finali (":").

    Di seguito è riportato un esempio di mapping delle annotazioni per le proprietà state e Role di una casella di controllo in una visualizzazione elenco o in un controllo di visualizzazione ad albero. Nella vista sono presenti due elementi che rappresentano le caselle di controllo e ognuna contiene immagini corrispondenti allo stato selezionato e non selezionato.

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    Per i valori di ruolo e stato validi, vedere la pagina relativa ai [ruoli oggetto](object-roles.md) e alle [costanti di stato dell'oggetto](object-state-constants.md).

    Il valore di indice può essere negativo quando si esegue il mapping delle proprietà per un controllo dispositivo di scorrimento.

    Quando si esegue il mapping di una proprietà Value o Description, il risultato è una stringa. Le stringhe non sono racchiuse tra virgolette e i due punti fungono da delimitatori.

    Per altre informazioni, vedere [formato della mappa delle annotazioni](value-map-annotation.md).

2.  **Creare il gestore di annotazioni e ottenere un puntatore alla relativa** interfaccia [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**

    Di seguito è riportato un esempio di come creare il gestore di annotazioni.

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  **Alleghi la stringa di mapping al controllo.**

    Chiamare [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passando l' **HWND** del controllo e un puntatore alla stringa di mapping.

    Il parametro *IdProp* sarà uno dei seguenti.

    

    | Parametro                   | Usato per                                                |
    |-----------------------------|---------------------------------------------------------|
    | \_ROLEMAP MSAAPROPID         | Per impostare una mappa dei ruoli per i controlli visualizzazione elenco o visualizzazione albero.  |
    | \_STATEMAP MSAAPROPID        | Per impostare una mappa di stato per i controlli visualizzazione elenco o visualizzazione albero. |
    | \_DESCRIPTIONMAP ACC \_ propid | Per impostare una mappa di descrizione per la visualizzazione elenco o le visualizzazioni albero.   |
    | \_VALUEMAP MSAAPROPID        | Per impostare una mappa di valori nei controlli dispositivo di scorrimento.                  |

    

     

4.  **Pulisci.**

    Prima di eliminare i controlli con annotazioni della mappa dei valori (ad esempio, quando si gestisce la [ \_ distruzione WM](../winmsg/wm-destroy.md)), è necessario deselezionare le proprietà precedentemente registrate e rilasciare il gestore di annotazioni.

    A tale scopo, chiamare [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) in base alle esigenze e rilasciare il puntatore su [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).

Per il codice di esempio, vedere [esempio di annotazione della mappa dei valori](value-map-annotation-sample.md).

 

 