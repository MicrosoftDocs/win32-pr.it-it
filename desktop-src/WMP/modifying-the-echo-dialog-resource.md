---
title: Modifica della risorsa finestra di dialogo Echo
description: Modifica della risorsa finestra di dialogo Echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Windows Media Player plug-in, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione del segnale digitale,pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, risorsa finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37dc88fe2c1b85dfc08727a00e744f1c5c16a2f25a4c5d429b2ab13898b0fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996141"
---
# <a name="modifying-the-echo-dialog-resource"></a>Modifica della risorsa finestra di dialogo Echo

È necessario modificare la risorsa finestra di dialogo che rappresenta l'interfaccia utente per l'oggetto della pagina delle proprietà. È prima di tutto possibile modificare la casella di modifica e l'etichetta esistenti in modo che siano utili per la proprietà delay time e quindi aggiungere una seconda casella di modifica e un'etichetta per la proprietà wet mix.

Per modificare la risorsa finestra di dialogo in Visual C++:

1.  Fare clic **sulla scheda ResourceView** nell'area Project lavoro.
2.  Espandere l'albero delle risorse aprendo la cartella di primo livello.
3.  Aprire la **cartella Finestra di** dialogo.
4.  Fare doppio clic sul nome della risorsa della finestra di dialogo, IDD \_ ECHOPROPPAGE. L'editor di risorse viene visualizzato nel riquadro di destra.

## <a name="changing-the-existing-resources"></a>Modifica delle risorse esistenti

Per modificare le risorse della pagina delle proprietà esistenti per la proprietà delay time:

1.  Modificare prima di tutto il testo nel controllo testo statico esistente. Fare clic con il pulsante destro del mouse sul controllo e quindi **scegliere Proprietà**. Nel campo **Didascalia** digitare la nuova didascalia:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Chiudere la finestra di dialogo Proprietà testo .
3.  Modificare ora il nome del controllo casella di modifica. A tale scopo, fare clic con il pulsante destro del mouse sul controllo e quindi scegliere **Proprietà**. Nel campo **ID** digitare un nuovo nome per il controllo:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Chiudere la finestra di dialogo Modifica proprietà .
5.  Salvare la risorsa.
6.  Risposta **Sì** se viene richiesto di ricaricare il file resource.h.
7.  Fare clic **sulla scheda FileView** nell'area Project lavoro. Aprire resource.h
8.  Individuare la definizione per la risorsa della casella di modifica del fattore di \# scala (IDC \_ SCALEFACTOR) ed eliminarla. Deve avere lo stesso numero ID di IDC \_ DELAYTIME.

## <a name="adding-the-new-resources"></a>Aggiunta delle nuove risorse

Per aggiungere le nuove risorse della pagina delle proprietà per la proprietà wet mix:

1.  Fare clic **sulla scheda ResourceView** nell'area Project per selezionarla.
2.  Fare doppio clic sul nome della finestra di dialogo della pagina delle proprietà, IDD \_ ECHOPROPPAGE. L'editor di risorse viene visualizzato nel riquadro di destra.
3.  Usare la casella degli strumenti per aggiungere un controllo testo statico e una casella di modifica alla pagina delle proprietà.
4.  Fare clic con il pulsante destro del mouse sul controllo testo statico e scegliere **Proprietà**.
5.  Digitare un nuovo nome per il controllo testo statico nel **campo ID:**
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Digitare una didascalia per l'etichetta:
    ```C++
    Effect level (%):
    
    ```

    

7.  Chiudere la finestra di dialogo Proprietà testo .
8.  Fare clic con il pulsante destro del mouse sulla casella di modifica e **scegliere Proprietà**.
9.  Digitare un nuovo nome per la casella di modifica nel **campo ID:**
    ```C++
    IDC_WETMIX
    
    ```

    

10. Chiudere la finestra di dialogo Modifica proprietà .

Quando si salva il progetto, potrebbe essere richiesto di ricaricare resource.h. In **questo caso,** fare clic su Sì. L'editor delle risorse della finestra di dialogo deve aggiungere i nomi delle risorse e i numeri ID a resource.h per gli elementi aggiunti. Se per qualche motivo questo non accade, è necessario aprire resource.h e digitare nuove voci per il controllo etichetta e casella di modifica e assegnare a ogni un numero ID univoco.

## <a name="modifying-and-adding-the-string-resources"></a>Modifica e aggiunta delle risorse stringa

Il codice di esempio della procedura guidata plug-in specifica una risorsa stringa denominata IDS SCALERANGEERROR che contiene un messaggio da visualizzare quando \_ l'input dell'utente non è compreso nell'intervallo. È possibile modificare questa risorsa in base alle proprie esigenze per il valore di tempo di ritardo seguendo questa procedura in Visual C++:

1.  Fare clic **sulla scheda ResourceView.**
2.  Aprire la **cartella Tabella** di stringhe.
3.  Fare doppio clic **sull'icona Tabella** di stringhe per aprire l'editor di risorse.
4.  Fare doppio clic sul nome della risorsa da modificare, in questo caso IDS \_ SCALERANGEERROR. Verrà visualizzata la finestra di dialogo Proprietà stringa .
5.  Modificare il nome nel **campo ID** in IDS \_ DELAYRANGEERROR.
6.  Modificare il testo nel **campo Didascalia:**
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Chiudere la finestra di dialogo Proprietà stringa .

Aggiungere quindi una nuova risorsa stringa per il messaggio di errore della proprietà wet mix.

1.  Fare doppio clic sulla riga vuota nella parte inferiore dell'editor di risorse.
2.  Modificare il nome nel **campo ID** in IDS \_ MIXRANGEERROR.
3.  Aggiungere il testo seguente al **campo Didascalia:**
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Chiudere la finestra di dialogo Proprietà stringa .

Esistono altri due valori da modificare nella tabella delle stringhe. IDS FRIENDLYNAME è il nome visualizzato nell'interfaccia Windows Media Player \_ utente per identificare il plug-in. IDS \_ DESCRIPTION consente di indicare all'utente il plug-in. Entrambe queste stringhe vengono passate come parametri alla funzione **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin,** chiamata nel metodo DllRegisterServer in Echodll.cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




