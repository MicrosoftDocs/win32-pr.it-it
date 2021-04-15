---
title: Informazioni sul progetto personalizzato
description: Questa sezione contiene informazioni generali sulla funzionalità di personalizzazione personalizzata e fornisce una panoramica concettuale del modo in cui un'applicazione può supportare il progetto personalizzato.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121a4df5aa6fab222a5c4387ebdcfba51a7977b2
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474552"
---
# <a name="about-custom-draw"></a>Informazioni sul progetto personalizzato

Questa sezione contiene informazioni generali sulla funzionalità di personalizzazione personalizzata e fornisce una panoramica concettuale del modo in cui un'applicazione può supportare il progetto personalizzato. Attualmente, i controlli seguenti supportano la funzionalità di estrazione personalizzata:

-   Controlli intestazione
-   Controlli elenco-visualizzazione
-   Controlli Rebar
-   Controlli della barra degli strumenti
-   Controlli ToolTip
-   Controlli TrackBar
-   Controlli di visualizzazione albero

<!-- -->

-   [Informazioni sui messaggi di notifica di estrazione personalizzata](#about-custom-draw-notification-messages)
-   [Cicli di verniciatura, fasi di disegno e messaggi di notifica](#paint-cycles-drawing-stages-and-notification-messages)
-   [Sfrutta i vantaggi dei servizi di creazione personalizzati](#taking-advantage-of-custom-draw-services)
    -   [Risposta alla notifica di PrePaint](#responding-to-the-prepaint-notification)
    -   [Richiesta di notifiche specifiche dell'elemento](#requesting-item-specific-notifications)
    -   [Disegno dell'elemento manualmente](#drawing-the-item-yourself)
    -   [Modifica di tipi di carattere e colori](#changing-fonts-and-colors)
-   [Progetto personalizzato con controlli List-View e Tree-View](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Progetto personalizzato con controlli List-View](#custom-draw-with-list-view-controls)
-   [Argomenti correlati](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>Informazioni sui messaggi di notifica di estrazione personalizzata

Tutti i controlli comuni che supportano il disegno personalizzato inviano i codici di notifica [ \_ CUSTOMDRAW](nm-customdraw.md) in punti specifici durante le operazioni di disegno. Questi codici di notifica descrivono le operazioni di disegno che si applicano all'intero controllo, nonché le operazioni di disegno specifiche per gli elementi all'interno del controllo. Analogamente a molti codici di notifica, le \_ notifiche CUSTOMDRAW di nm vengono inviate come messaggi di [**\_ notifica WM**](wm-notify.md) .

Il parametro *lParam* di una notifica di progetto personalizzata sarà l'indirizzo di una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) o una struttura specifica del controllo che contiene una struttura **NMCUSTOMDRAW** come primo membro. Nella tabella seguente viene illustrata la relazione tra i controlli e le strutture utilizzate.



| Struttura                                | Usato da                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Controlli Rebar, TrackBar e header |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Controlli elenco-visualizzazione                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Controlli della barra degli strumenti                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Controlli ToolTip                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Controlli di visualizzazione albero                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Cicli di verniciatura, fasi di disegno e messaggi di notifica

Come tutte le applicazioni Windows, i controlli comuni disegnano e cancellano periodicamente in base ai messaggi ricevuti dal sistema o da altre applicazioni. Il processo di disegno o cancellazione di un controllo viene definito ciclo di *disegno*. I controlli che supportano il disegno personalizzato inviano periodicamente i codici di notifica [ \_ CUSTOMDRAW](nm-customdraw.md) per ogni ciclo di disegno. Questo codice di notifica è accompagnato da una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) o da un'altra struttura che contiene una struttura **NMCUSTOMDRAW** come primo membro.

Una parte delle informazioni contenute nella struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è la fase corrente del ciclo di disegno. Questa operazione viene definita fase di *estrazione* ed è rappresentata dal valore nel membro **dwDrawStage** della struttura. Un controllo informa l'elemento padre su quattro fasi di estrazione di base. Queste fasi di traccia di base o globali sono rappresentate nella struttura con i valori di flag seguenti (definiti in commctrl. h).



| Valori della fase di estrazione globale | Descrizione                        |
|--------------------------|------------------------------------|
| CDDS \_ PREpaint           | Prima dell'inizio del ciclo di disegno.     |
| CDDS \_ POSTpaint          | Al termine del ciclo di disegno. |
| precancellazione CDDS \_           | Prima dell'inizio del ciclo di cancellazione.     |
| CDDS \_ POSTerase          | Al termine del ciclo di cancellazione. |



 

Ognuno dei valori precedenti può essere combinato con il flag di \_ elemento CDDS per specificare le fasi di traccia specifiche degli elementi. Per praticità, COMmctrl. h contiene i valori specifici dell'elemento seguenti.



| Valori della fase di traccia specifici dell'elemento | Descrizione                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ITEMPREPAINT CDDS              | Prima della traccia di un elemento.                                                                                                                                                                                                                                                            |
| \_ITEMPOSTPAINT CDDS             | Dopo la traccia di un elemento.                                                                                                                                                                                                                                                       |
| \_ITEMPREERASE CDDS              | Prima della cancellazione di un elemento.                                                                                                                                                                                                                                                           |
| \_ITEMPOSTERASE CDDS             | Dopo la cancellazione di un elemento.                                                                                                                                                                                                                                                      |
| sottoelemento CDDS \_                   | [Versioni di controllo comuni](common-control-versions.md) 4,71. Flag combinato con CDDS \_ ITEMPREPAINT o CDDS \_ ITEMPOSTPAINT se viene disegnato un sottoelemento. Questa impostazione verrà impostata solo se viene restituito [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) da CDDS \_ PrePaint. |



 

L'applicazione deve elaborare il codice di notifica [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) e quindi restituire un valore specifico che informa il controllo cosa deve fare. Per ulteriori informazioni su questi valori restituiti, vedere le sezioni seguenti.

## <a name="taking-advantage-of-custom-draw-services"></a>Sfrutta i vantaggi dei servizi di creazione personalizzati

La chiave per sfruttare la funzionalità di estrazione personalizzata è la risposta ai codici di notifica [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) inviati da un controllo. I valori restituiti che l'applicazione invia in risposta a queste notifiche determinano il comportamento del controllo per il ciclo di disegno.

Questa sezione contiene informazioni sul modo in cui l'applicazione può usare i valori restituiti della notifica [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) per determinare il comportamento del controllo.

I dettagli sono suddivisi negli argomenti seguenti:

-   [Risposta alla notifica di PrePaint](#responding-to-the-prepaint-notification)
-   [Richiesta di notifiche specifiche dell'elemento](#requesting-item-specific-notifications)
-   [Disegno dell'elemento manualmente](#drawing-the-item-yourself)
-   [Modifica di tipi di carattere e colori](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Risposta alla notifica di PrePaint

All'inizio di ogni ciclo di disegno, il controllo Invia il codice di notifica [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) , specificando il \_ valore di PrePaint CDDS nel membro **dwDrawStage** della struttura di Nm \_ CUSTOMDRAW associata. Il valore restituito dall'applicazione a questa prima notifica determina come e quando il controllo Invia notifiche di disegno personalizzate successive per il resto del ciclo di disegno. L'applicazione può restituire una combinazione dei flag seguenti in risposta alla prima notifica.



| Valore restituito            | Effetto                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_DODEFAULT CDRF         | Il controllo viene disegnato automaticamente. Non invierà altre notifiche [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) per questo ciclo di disegno. Questo flag non può essere usato con altri flag.                                                                                                                                                                                                                                                                               |
| \_DOERASE CDRF           | Il controllo trarrà solo lo sfondo.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \_NEWFONT CDRF           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](#changing-fonts-and-colors). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                       |
| \_NOTIFYITEMDRAW CDRF    | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno specifica dell'elemento. Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo aver disegnato gli elementi. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.                                                                                                                                                                                                                       |
| \_NOTIFYPOSTERASE CDRF   | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.                                                                                                                                                                                                                                                                                                                                             |
| \_NOTIFYPOSTPAINT CDRF   | Il controllo invierà una [notifica \_ CUSTOMDRAW Nm](nm-customdraw.md) quando il ciclo di disegno per l'intero controllo è completo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.                                                                                                                                                                                                                                                                 |
| \_NOTIFYSUBITEMDRAW CDRF | [Versione 4,71](common-control-versions.md). L'applicazione riceverà una notifica [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT \| CDDS \_ sottoelemento prima che ogni elemento secondario di visualizzazione elenco venga disegnato. È quindi possibile specificare il tipo di carattere e il colore per ogni elemento secondario separatamente oppure restituire [**CDRF \_ DODEFAULT**](cdrf-constants.md) per l'elaborazione predefinita. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT. |
| \_SKIPDEFAULT CDRF       | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                                                                                                                                      |
| \_SKIPPOSTPAINT CDRF     | Il controllo non trarrà il rettangolo di attivazione intorno a un elemento.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Richiesta di notifiche specifiche dell'elemento

Se l'applicazione restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) alla notifica di disegno personalizzata di PrePaint iniziale, il controllo invierà notifiche per ogni elemento disegnato durante il ciclo di disegno. Queste notifiche specifiche dell'elemento avranno il \_ valore ITEMPREPAINT di CDDS nel membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata. È possibile richiedere che il controllo invii un'altra notifica al termine del disegno dell'elemento restituendo [**CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) a queste notifiche specifiche dell'elemento. In caso contrario, restituire [**CDRF \_ DODEFAULT**](cdrf-constants.md) e il controllo non invierà una notifica alla finestra padre fino a quando non inizierà a tracciare l'elemento successivo.

### <a name="drawing-the-item-yourself"></a>Disegno dell'elemento manualmente

Se l'applicazione disegna l'intero elemento, restituire [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md). Ciò consente al controllo di ignorare gli elementi che non è necessario creare, riducendo in tal modo l'overhead del sistema. Tenere presente che la restituzione di questo valore indica che il controllo non trarrà alcuna parte dell'elemento.

### <a name="changing-fonts-and-colors"></a>Modifica di tipi di carattere e colori

L'applicazione può usare il progetto personalizzato per modificare il tipo di carattere di un elemento. È sufficiente selezionare il HFONT che si vuole inserire nel contesto di dispositivo specificato dal membro **HDC** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata alla notifica di estrazione personalizzata. Poiché il tipo di carattere selezionato potrebbe avere metriche diverse da quelle del tipo di carattere predefinito, assicurarsi di includere il bit [**CDRF \_ NEWFONT**](cdrf-constants.md) nel valore restituito per il messaggio di notifica. Per altre informazioni sull'uso di questa funzionalità, vedere il codice di esempio in uso di un [progetto personalizzato](using-custom-draw.md). Il tipo di carattere specificato dall'applicazione viene utilizzato per visualizzare l'elemento quando non è selezionato. Il progetto personalizzato non consente di modificare gli attributi del tipo di carattere per gli elementi selezionati.

Per modificare i colori del testo per tutti i controlli che supportano l'estrazione personalizzata, ad eccezione della visualizzazione elenco e della visualizzazione albero, è sufficiente impostare il testo e i colori di sfondo desiderati nel contesto di dispositivo fornito nella struttura di notifica di estrazione personalizzata con le funzioni [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) e [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) . Per modificare i colori del testo nella visualizzazione elenco o nella visualizzazione albero, è necessario inserire i valori dei colori desiderati nei membri **clrText** e **ClrTextBk** della struttura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) o [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) .

> [!Note]  
> Prima della [versione 6,0](common-control-versions.md) dei controlli comuni, le barre degli strumenti ignoravano il flag [**\_ NEWFONT di CDRF**](cdrf-constants.md) . La versione 6,0 supporta il flag **CDRF \_ NEWFONT** ed è possibile usarla per selezionare un tipo di carattere diverso per la barra degli strumenti. Tuttavia, non è possibile modificare il colore di una barra degli strumenti quando è attivo uno stile di visualizzazione. Per modificare il colore di una barra degli strumenti nella versione 6,0, è necessario innanzitutto disabilitare gli stili di visualizzazione chiamando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) e specificando nessun stile di visualizzazione:

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Progetto personalizzato con controlli List-View e Tree-View

La maggior parte dei controlli comuni può essere gestita essenzialmente nello stesso modo. Tuttavia, i controlli visualizzazione elenco e visualizzazione albero dispongono di alcune funzionalità che richiedono un approccio leggermente diverso al progetto personalizzato.

Per la [versione 5,0](common-control-versions.md), questi due controlli possono visualizzare il testo ritagliato se si modifica il tipo di carattere restituendo [**CDRF \_ NEWFONT**](cdrf-constants.md). Questo comportamento è necessario per garantire la compatibilità con le versioni precedenti dei controlli comuni. Se si desidera modificare il tipo di carattere di un controllo visualizzazione elenco o visualizzazione albero, si otterranno risultati migliori se si invia un messaggio di [**tipo \_ CCM**](ccm-setversion.md) con il valore *wParam* impostato su 5 prima di aggiungere elementi al controllo. Per un esempio di controllo di visualizzazione albero che usa il modello di illustrazione personalizzato, vedere l'articolo della Knowledge base [esempio: CustDTv illustra il progetto personalizzato in un oggetto TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496).

### <a name="custom-draw-with-list-view-controls"></a>Progetto personalizzato con controlli List-View

Poiché i controlli elenco-visualizzazione includono elementi secondari e più modalità di visualizzazione, è necessario gestire la [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) in modo leggermente diverso rispetto agli altri controlli comuni.

Per la modalità report, utilizzare la procedura riportata di seguito.

1.  La prima [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) avrà il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata impostata su CDDS \_ PrePaint. Restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Si riceverà quindi una notifica [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT. Se si specificano nuovi tipi di carattere o colori e si restituisce [**CDRF \_ NEWFONT**](cdrf-constants.md), verranno modificati tutti gli elementi secondari dell'elemento. Se invece si desidera gestire ogni elemento secondario separatamente, restituire [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md).
3.  Se nel passaggio precedente è stato restituito [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md) , si riceverà una notifica [di \_ CUSTOMDRAW Nm](nm-customdraw.md) per ogni elemento secondario con **dwDrawStage** impostato su CDDS \_ sottoelemento CDDS ITEMPREPAINT \| \_ . Per modificare il tipo di carattere o il colore dell'elemento secondario, specificare un nuovo tipo di carattere o colore e restituire [**CDRF \_ NEWFONT**](cdrf-constants.md).

Per l'icona grande, l'icona piccola e le modalità elenco, utilizzare la procedura riportata di seguito.

1.  La prima [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) avrà il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata impostata su CDDS \_ PrePaint. Restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Si riceverà quindi una notifica [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT. È possibile modificare i tipi di carattere o i colori di un elemento specificando nuovi tipi di carattere e colori e restituendo [**CDRF \_ NEWFONT**](cdrf-constants.md). Poiché queste modalità non dispongono di elementi secondari, non si riceveranno altre \_ notifiche CUSTOMDRAW di nm.

Per un esempio di gestore di notifiche [ \_ CUSTOMDRAW](nm-customdraw.md) di visualizzazione elenco, vedere uso di un [progetto personalizzato](using-custom-draw.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso di un progetto personalizzato](using-custom-draw.md)
</dt> <dt>

[Riferimento di progetto personalizzato](custom-draw-reference.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[ESEMPIO: CustDTv illustra il progetto personalizzato in un oggetto TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 