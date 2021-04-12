---
title: Aggiunta e modifica degli eventi
description: Aggiunta e modifica degli eventi
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331132"
---
# <a name="adding-and-modifying-the-events"></a>Aggiunta e modifica degli eventi

È necessario fornire gestori eventi per gli \_ eventi di modifica it che si verificano quando l'utente modifica il testo nelle caselle di modifica della pagina delle proprietà. Questi gestori di eventi hanno un'implementazione semplice che consente di **applicare** solo la finestra di dialogo della pagina delle proprietà.

## <a name="modifying-the-scale-factor-event-handler"></a>Modifica del gestore eventi del fattore di scala

È necessario modificare il nome del gestore eventi esistente fornito dalla procedura guidata plug-in per la casella di modifica fattore di scala. È necessario modificare il nome da OnChangeScale a OnChangeDelay in tre posizioni:

1.  In EchoPropPage. h, modificare il nome nella sezione della macro della mappa messaggi. Sostituire la riga che esegue il mapping dell'evento di modifica del fattore di scala al metodo OnChangeScale con il codice seguente:
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  In EchoPropPage. h modificare il nome nella riga che prototipa la funzione OnChangeScale:
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  In EchoPropPage. cpp modificare il nome nell'intestazione della funzione:
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Aggiunta del gestore dell'evento Wet Mix

È possibile aggiungere facilmente il gestore eventi per l' \_ evento di modifica en associato al \_ controllo della casella di modifica IDC WETMIX. Dall'editor di risorse della finestra di dialogo:

1.  Fare clic con il pulsante destro del mouse sulla \_ casella di modifica IDC WETMIX e scegliere **eventi**. Verrà visualizzata la finestra di dialogo nuovo messaggio e gestori eventi di Windows.
2.  Nella casella **classe o oggetto da gestire** , fare clic sul nome della risorsa casella di modifica, IDC \_ WETMIX.
3.  Nella casella **New Windows Messages/Events** fare clic su en \_ Change per selezionarlo.
4.  Fare clic su **Aggiungi gestore**. Verrà visualizzata la finestra di dialogo Aggiungi funzione membro.
5.  Nella casella **nome funzione membro** Digitare il nome OnChangeWetmix.
6.  Fare clic su **OK** per chiudere la finestra di dialogo Aggiungi funzione membro.
7.  Fare clic su **OK** per tornare all'editor risorse della finestra di dialogo.

Visual C++ aggiunge automaticamente il codice per la mappa messaggi e la funzione del gestore eventi a EchoPropPage. h. Il codice inserito fornisce un commento TODO in cui è possibile aggiungere l'implementazione nell'intestazione per la funzione. Si tratta di uno stile leggermente diverso rispetto a quello usato dal codice di esempio della procedura guidata per il plug-in di Windows Media Player, ma è accettabile.

Se si desidera scrivere l'implementazione nel file di intestazione o spostarla in EchoPropPage. cpp, è possibile. In entrambi i casi, l'implementazione richiede solo una singola riga di codice aggiuntiva per abilitare **applica** nella finestra di dialogo della pagina delle proprietà. Inserire questa riga di codice prima della riga restituita dalla funzione:


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica della pagina delle proprietà di esempio Echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




