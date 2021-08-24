---
title: Aggiunta e modifica degli eventi
description: Aggiunta e modifica degli eventi
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Windows Media Player plug-in, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione del segnale digitale,pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP,eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 464d20b600a5535e3cf2c02be01fa19c10a590e143c7a96375580719b70c274c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865341"
---
# <a name="adding-and-modifying-the-events"></a>Aggiunta e modifica degli eventi

È necessario fornire gestori eventi per gli eventi EN CHANGE che si verificano quando l'utente modifica il testo nelle caselle di modifica \_ della pagina delle proprietà. Questi gestori eventi hanno una semplice implementazione che abilita **semplicemente Apply** nella finestra di dialogo della pagina delle proprietà.

## <a name="modifying-the-scale-factor-event-handler"></a>Modifica del gestore dell'evento Scale Factor

È necessario modificare il nome del gestore eventi esistente fornito dalla procedura guidata del plug-in per la casella di modifica del fattore di scala. È necessario modificare il nome da OnChangeScale a OnChangeDelay in tre posizioni:

1.  In EchoPropPage.h modificare il nome nella sezione della macro della mappa messaggi. Sostituire la riga che esegue il mapping dell'evento di modifica del fattore di scala al metodo OnChangeScale con il codice seguente:
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  In EchoPropPage.h modificare il nome nella riga che prototipa la funzione OnChangeScale:
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  In EchoPropPage.cpp modificare il nome nell'intestazione della funzione:
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Aggiunta del gestore dell'evento Wet Mix

È possibile aggiungere facilmente il gestore eventi per l'evento EN CHANGE associato al controllo della casella di modifica \_ \_ IDC WETMIX. Nell'editor delle risorse della finestra di dialogo:

1.  Fare clic con il pulsante destro del mouse sulla casella di modifica IDC \_ WETMIX e scegliere **Eventi**. Verrà visualizzata Windows finestra di dialogo Nuovo messaggio e gestori eventi.
2.  Nella casella **Classe o oggetto da gestire** fare clic sul nome della risorsa della casella di modifica, IDC \_ WETMIX.
3.  Nella casella **Nuovo Windows messaggi/eventi** fare clic su EN \_ CHANGE per selezionarlo.
4.  Fare clic **su Aggiungi gestore**. Verrà visualizzata la finestra di dialogo Aggiungi funzione membro .
5.  Nella casella **Nome funzione membro** digitare il nome OnChangeWetmix.
6.  Fare **clic su OK** per chiudere la finestra di dialogo Aggiungi funzione membro .
7.  Fare **clic su OK** per tornare all'editor delle risorse della finestra di dialogo.

Visual C++ aggiunge automaticamente il codice per la mappa messaggi e per la funzione del gestore eventi a EchoPropPage.h. Il codice inserito fornisce un commento TODO in cui è possibile aggiungere l'implementazione nell'intestazione per la funzione. Si tratta di uno stile leggermente diverso da quello Windows Media Player codice di esempio della Creazione guidata plug-in, ma è accettabile.

È possibile scrivere l'implementazione nel file di intestazione o spostarla in EchoPropPage.cpp. In entrambi i casi, l'implementazione richiede una sola riga di codice aggiuntiva per abilitare **Applica** nella finestra di dialogo della pagina delle proprietà. Inserire questa riga di codice prima della riga restituita dalla funzione:


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




