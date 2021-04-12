---
title: Modifica della risorsa della finestra di dialogo Echo
description: Modifica della risorsa della finestra di dialogo Echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, risorsa finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331207"
---
# <a name="modifying-the-echo-dialog-resource"></a>Modifica della risorsa della finestra di dialogo Echo

È necessario modificare la risorsa della finestra di dialogo che rappresenta l'interfaccia utente per l'oggetto pagina delle proprietà. È possibile modificare prima di tutto la casella di modifica e l'etichetta esistenti in modo da essere utile per la proprietà delay time, quindi aggiungere una seconda casella di modifica ed etichetta per la proprietà Wet Mix.

Per modificare la risorsa finestra di dialogo in Visual C++:

1.  Fare clic sulla scheda **ResourceView** nell'area di lavoro progetto.
2.  Espandere l'albero delle risorse aprendo la cartella di livello superiore.
3.  Aprire la cartella della **finestra di dialogo** .
4.  Fare doppio clic sul nome della risorsa della finestra di dialogo, IDD \_ ECHOPROPPAGE. L'editor risorse verrà visualizzato nel riquadro di destra.

## <a name="changing-the-existing-resources"></a>Modifica delle risorse esistenti

Per modificare le risorse della pagina delle proprietà esistenti per la proprietà tempo di ritardo:

1.  Per prima cosa, modificare il testo nel controllo testo statico esistente. Fare clic con il pulsante destro del mouse sul controllo e scegliere **Proprietà**. Nel campo **didascalia** Digitare la nuova didascalia:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Chiudere la finestra di dialogo Proprietà testo.
3.  A questo punto, modificare il nome del controllo casella di modifica. A tale scopo, fare clic con il pulsante destro del mouse sul controllo e scegliere **Proprietà**. Nel campo **ID** Digitare un nuovo nome per il controllo:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Chiudere la finestra di dialogo Modifica proprietà.
5.  Salvare la risorsa.
6.  Risposta **Sì** se viene richiesto di ricaricare il file Resource. h.
7.  Fare clic sulla scheda **FileView** nell'area di lavoro progetto. Apri Resource. h
8.  Individuare l'oggetto \# define per la risorsa della casella di modifica del fattore di scala (IDC \_ SCALEFACTOR) ed eliminarlo. Deve avere lo stesso numero ID di IDC \_ DELAYTIME.

## <a name="adding-the-new-resources"></a>Aggiunta di nuove risorse

Per aggiungere le nuove risorse della pagina delle proprietà per la proprietà Wet Mix:

1.  Fare clic sulla scheda **ResourceView** nell'area di lavoro del progetto per selezionarla.
2.  Fare doppio clic sul nome della finestra di dialogo pagina delle proprietà, IDD \_ ECHOPROPPAGE. L'editor risorse verrà visualizzato nel riquadro di destra.
3.  Utilizzare la casella degli strumenti per aggiungere un controllo testo statico e una casella di modifica alla pagina delle proprietà.
4.  Fare clic con il pulsante destro del mouse sul controllo testo statico e scegliere **Proprietà**.
5.  Digitare un nuovo nome per il controllo testo statico nel campo **ID** :
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Digitare una didascalia per l'etichetta:
    ```C++
    Effect level (%):
    
    ```

    

7.  Chiudere la finestra di dialogo Proprietà testo.
8.  Fare clic con il pulsante destro del mouse sulla casella di modifica e scegliere **Proprietà**.
9.  Digitare un nuovo nome per la casella di modifica nel campo **ID** :
    ```C++
    IDC_WETMIX
    
    ```

    

10. Chiudere la finestra di dialogo Modifica proprietà.

Quando si salva il progetto, potrebbe essere richiesto di ricaricare Resource. h. Se ciò accade, fare clic su **Sì** . L'editor risorse della finestra di dialogo deve aggiungere i nomi delle risorse e i numeri ID a Resource. h per gli elementi aggiunti. Se per qualche motivo questa operazione non viene eseguita, è necessario aprire Resource. h e digitare le nuove voci per il controllo etichetta e casella di modifica e assegnare ogni numero ID univoco.

## <a name="modifying-and-adding-the-string-resources"></a>Modifica e aggiunta di risorse di stringa

Il codice di esempio della procedura guidata plug-in specifica una risorsa stringa denominata ID \_ SCALERANGEERROR che contiene un messaggio da visualizzare quando l'input dell'utente non è compreso nell'intervallo. È possibile modificare questa risorsa per adattarla alle proprie esigenze per il valore di tempo di ritardo attenendosi alla procedura descritta in Visual C++:

1.  Fare clic sulla scheda **ResourceView** .
2.  Aprire la cartella della **tabella di stringhe** .
3.  Fare doppio clic sull'icona della **tabella di stringhe** per aprire l'editor risorse.
4.  Fare doppio clic sul nome della risorsa che si desidera modificare, in questo caso ID \_ SCALERANGEERROR. Verrà visualizzata la finestra di dialogo Proprietà stringa.
5.  Modificare il nome nel campo **ID** in ID \_ DELAYRANGEERROR.
6.  Modificare il testo nel campo **didascalia** :
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Chiudere la finestra di dialogo Proprietà stringa.

Successivamente, aggiungere una nuova risorsa di stringa per il messaggio di errore della proprietà Wet Mix.

1.  Fare doppio clic sulla riga vuota nella parte inferiore dell'editor risorse.
2.  Modificare il nome nel campo **ID** in ID \_ MIXRANGEERROR.
3.  Aggiungere il testo seguente al campo **didascalia** :
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Chiudere la finestra di dialogo Proprietà stringa.

Esistono altri due valori che si desidera modificare nella tabella delle stringhe. IDS \_ FriendlyName è il nome visualizzato nell'interfaccia utente di Windows Media Player per identificare il plug-in. \_Descrizione ID consente di comunicare all'utente il plug-in. Entrambe queste stringhe vengono passate come parametri alla funzione **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** , che viene chiamata nel metodo DllRegisterServer in Echodll. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà di esempio Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




