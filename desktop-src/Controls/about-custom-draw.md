---
title: Informazioni sul disegno personalizzato
description: Questa sezione contiene informazioni generali sulla funzionalità di disegno personalizzato e offre una panoramica concettuale del modo in cui un'applicazione può supportare il disegno personalizzato.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4961d80c04f8fa570286666511c04b1208c940369cd13b836095b8899505de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922491"
---
# <a name="about-custom-draw"></a>Informazioni sul disegno personalizzato

Questa sezione contiene informazioni generali sulla funzionalità di disegno personalizzato e offre una panoramica concettuale del modo in cui un'applicazione può supportare il disegno personalizzato. Attualmente, i controlli seguenti supportano la funzionalità di disegno personalizzato:

-   Controlli intestazione
-   Controlli di visualizzazione elenco
-   Controlli Rebar
-   Controlli della barra degli strumenti
-   Controlli della descrizione comando
-   Controlli Trackbar
-   Controlli di visualizzazione albero

<!-- -->

-   [Informazioni sui messaggi di notifica di disegno personalizzati](#about-custom-draw-notification-messages)
-   [Paint Cicli, fasi di disegno e messaggi di notifica](#paint-cycles-drawing-stages-and-notification-messages)
-   [Sfruttare i servizi di disegno personalizzati](#taking-advantage-of-custom-draw-services)
    -   [Risposta alla notifica di pre-aggiornamento](#responding-to-the-prepaint-notification)
    -   [Richiesta di notifiche specifiche dell'elemento](#requesting-item-specific-notifications)
    -   [Disegno dell'elemento manualmente](#drawing-the-item-yourself)
    -   [Modifica di tipi di carattere e colori](#changing-fonts-and-colors)
-   [Disegno personalizzato con List-View e Tree-View personalizzati](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Disegno personalizzato con List-View personalizzati](#custom-draw-with-list-view-controls)
-   [Argomenti correlati](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>Informazioni sui messaggi di notifica di disegno personalizzati

Tutti i controlli comuni che supportano il disegno personalizzato [inviano codici di notifica \_ NM CUSTOMDRAW](nm-customdraw.md) in punti specifici durante le operazioni di disegno. Questi codici di notifica descrivono le operazioni di disegno che si applicano all'intero controllo, nonché le operazioni di disegno specifiche per gli elementi all'interno del controllo. Come molti codici di notifica, le notifiche DI NM \_ CUSTOMDRAW vengono inviate [**come messaggi WM \_ NOTIFY.**](wm-notify.md)

Il *parametro lParam* di una notifica di disegno personalizzata sarà l'indirizzo di una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) o di una struttura specifica del controllo che contiene una **struttura NMCUSTOMDRAW** come primo membro. Nella tabella seguente viene illustrata la relazione tra i controlli e le strutture usate.



| Struttura                                | Usato da                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Controlli rebar, trackbar e header |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Controlli di visualizzazione elenco                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Controlli della barra degli strumenti                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Controlli della descrizione comando                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Controlli di visualizzazione albero                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Paint Cicli, fasi di disegno e messaggi di notifica

Come tutte Windows, i controlli comuni disegnano e cancellano periodicamente se stessi in base ai messaggi ricevuti dal sistema o da altre applicazioni. Il processo di disegno o cancellazione di un controllo è detto *ciclo di disegno*. I controlli che supportano il disegno personalizzato [inviano \_ periodicamente codici di notifica NM CUSTOMDRAW](nm-customdraw.md) attraverso ogni ciclo di disegno. Questo codice di notifica è accompagnato da una [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) o da un'altra struttura che contiene **una struttura NMCUSTOMDRAW** come primo membro.

Una delle informazioni contenute nella [**struttura NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) è la fase corrente del ciclo di disegno. Questa fase viene definita fase *di* disegno ed è rappresentata dal valore nel membro **dwDrawStage della** struttura. Un controllo informa l'elemento padre su quattro fasi di disegno di base. Queste fasi di disegno di base o globali sono rappresentate nella struttura dai valori di flag seguenti (definiti in Commctrl.h).



| Valori globali della fase di disegno | Descrizione                        |
|--------------------------|------------------------------------|
| CDDS \_ PREPAINT           | Prima dell'inizio del ciclo di disegno.     |
| CDDS \_ POSTPAINT          | Al termine del ciclo di disegno. |
| CDDS \_ PREERASE           | Prima dell'inizio del ciclo di cancellazione.     |
| CDDS \_ POSTERASE          | Al termine del ciclo di cancellazione. |



 

Ognuno dei valori precedenti può essere combinato con il flag CDDS ITEM per specificare le \_ fasi di disegno specifiche degli elementi. Per praticità, Commctrl.h contiene i valori specifici dell'elemento seguenti.



| Valori della fase di disegno specifici dell'elemento | Descrizione                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ELEMENTO \_ CDDSPREPAINT              | Prima che venga disegnato un elemento.                                                                                                                                                                                                                                                            |
| CDDS \_ ITEMPOSTPAINT             | Dopo che un elemento è stato disegnato.                                                                                                                                                                                                                                                       |
| CDDS \_ ITEMPREERASE              | Prima della cancellazione di un elemento.                                                                                                                                                                                                                                                           |
| CDDS \_ ITEMPOSTERASE             | Dopo la cancellazione di un elemento.                                                                                                                                                                                                                                                      |
| ELEMENTO \_ SECONDARIO CDDS                   | [Versioni comuni del controllo](common-control-versions.md) 4.71. Flag combinato con CDDS \_ ITEMPREPAINT o CDDS \_ ITEMPOSTPAINT se viene disegnato un elemento secondario. Verrà impostato solo se [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) viene restituito da CDDS \_ PREPAINT. |



 

L'applicazione deve elaborare il codice di notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) e quindi restituire un valore specifico che informi il controllo che cosa deve fare. Per altre informazioni su questi valori restituiti, vedere le sezioni seguenti.

## <a name="taking-advantage-of-custom-draw-services"></a>Sfruttare i servizi di disegno personalizzati

La chiave per sfruttare la funzionalità di disegno personalizzato è rispondere ai codici di notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) inviati da un controllo. I valori restituiti inviati dall'applicazione in risposta a queste notifiche determinano il comportamento del controllo per tale ciclo di disegno.

Questa sezione contiene informazioni su come l'applicazione può usare i valori restituiti dalla notifica [ \_ NM CUSTOMDRAW](nm-customdraw.md) per determinare il comportamento del controllo.

I dettagli sono suddivisi negli argomenti seguenti:

-   [Risposta alla notifica di pre-aggiornamento](#responding-to-the-prepaint-notification)
-   [Richiesta di notifiche specifiche dell'elemento](#requesting-item-specific-notifications)
-   [Disegno dell'elemento manualmente](#drawing-the-item-yourself)
-   [Modifica di tipi di carattere e colori](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Risposta alla notifica di pre-aggiornamento

All'inizio di ogni ciclo di disegno, il controllo invia il codice di notifica [NM \_ CUSTOMDRAW,](nm-customdraw.md) specificando il valore CDDS PREPAINT nel membro \_ **dwDrawStage** della struttura NM \_ CUSTOMDRAW associato. Il valore restituito dall'applicazione a questa prima notifica determina come e quando il controllo invia notifiche di disegno personalizzate successive per il resto del ciclo di disegno. L'applicazione può restituire una combinazione dei flag seguenti in risposta alla prima notifica.



| Valore restituito            | Effetto                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDRF \_ DODEFAULT         | Il controllo disegna se stesso. Non invierà notifiche [AGGIUNTIVE DI NM \_ CUSTOMDRAW](nm-customdraw.md) per questo ciclo di disegno. Questo flag non può essere usato con altri flag.                                                                                                                                                                                                                                                                               |
| CDRF \_ DOERASE           | Il controllo disegna solo lo sfondo.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CDRF \_ NEWFONT           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo userà il nuovo tipo di carattere. Per altre informazioni sulla modifica dei tipi di carattere, vedere [Modifica di tipi di carattere e colori](#changing-fonts-and-colors). Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                       |
| CDRF \_ NOTIFYITEMDRAW    | Il controllo invierà una notifica all'elemento padre di qualsiasi operazione di disegno specifica dell'elemento. Invierà i [codici di notifica DI NM \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.                                                                                                                                                                                                                       |
| CDRF \_ NOTIFYPOSTERASE   | Il controllo invierà una notifica all'elemento padre dopo la cancellazione di un elemento. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.                                                                                                                                                                                                                                                                                                                                             |
| CDRF \_ NOTIFYPOSTPAINT   | Il controllo invierà una [notifica NM \_ CUSTOMDRAW](nm-customdraw.md) al termine del ciclo di disegno per l'intero controllo. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ PREPAINT.                                                                                                                                                                                                                                                                 |
| CDRF \_ NOTIFYSUBITEMDRAW | [Versione 4.71](common-control-versions.md). L'applicazione riceverà una [notifica NM \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT CDDS SUBITEM prima di disegnare ogni elemento secondario \| della visualizzazione \_ elenco. È quindi possibile specificare il tipo di carattere e il colore per ogni elemento secondario separatamente o restituire [**CDRF \_ DODEFAULT**](cdrf-constants.md) per l'elaborazione predefinita. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ ITEMPREPAINT. |
| SKIPDEFAULT DI CDRF \_       | L'applicazione ha creato l'elemento manualmente. Il controllo non disegna l'elemento. Ciò si verifica **quando dwDrawStage è** uguale a CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                                                                                                                                      |
| CDRF \_ SKIPPOSTPAINT     | Il controllo non disegna il rettangolo di attivazione intorno a un elemento.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Richiesta di notifiche specifiche dell'elemento

Se l'applicazione restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) alla notifica di disegno personalizzato di pre-disegno iniziale, il controllo invierà notifiche per ogni elemento che disegna durante il ciclo di disegno. Queste notifiche specifiche dell'elemento avranno il valore CDDS ITEMPREPAINT nel membro \_ **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che lo accompagna. È possibile richiedere che il controllo invii un'altra notifica al termine del disegno dell'elemento, restituindo [**CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) a queste notifiche specifiche dell'elemento. In caso contrario, restituisce [**CDRF \_ DODEFAULT**](cdrf-constants.md) e il controllo non invierà una notifica alla finestra padre finché non inizia a disegnare l'elemento successivo.

### <a name="drawing-the-item-yourself"></a>Disegno dell'elemento manualmente

Se l'applicazione disegna l'intero elemento, restituisce [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md). In questo modo il controllo può ignorare gli elementi che non è necessario disegnare, riducendo così il sovraccarico di sistema. Tenere presente che la restituzione di questo valore indica che il controllo non disegna alcuna parte dell'elemento.

### <a name="changing-fonts-and-colors"></a>Modifica di tipi di carattere e colori

L'applicazione può usare il disegno personalizzato per modificare il tipo di carattere di un elemento. È sufficiente selezionare il valore HFONT desiderato nel contesto di dispositivo specificato dal membro **hdc** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata alla notifica di disegno personalizzato. Poiché il tipo di carattere selezionato potrebbe avere metriche diverse rispetto al tipo di carattere predefinito, assicurarsi di includere il bit [**CDRF \_ NEWFONT**](cdrf-constants.md) nel valore restituito per il messaggio di notifica. Per altre informazioni sull'uso di questa funzionalità, vedere il codice di esempio in [Using Custom Draw](using-custom-draw.md). Il tipo di carattere specificato dall'applicazione viene usato per visualizzare l'elemento quando non è selezionato. Il disegno personalizzato non consente di modificare gli attributi del tipo di carattere per gli elementi selezionati.

Per modificare i colori del testo per tutti i controlli che supportano il disegno personalizzato, ad eccezione della visualizzazione elenco e della visualizzazione albero, è sufficiente impostare i colori di testo e di sfondo desiderati nel contesto di dispositivo fornito nella struttura di notifica di disegno personalizzato con le funzioni [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) e [**SetBkColor.**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) Per modificare i colori del testo nella visualizzazione elenco o nella visualizzazione albero, è necessario inserire i valori di colore desiderati nei membri **clrText** e **clrTextBk** della struttura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) o [**NMTVCUSTOMDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw)

> [!Note]  
> Prima della [versione 6.0 dei](common-control-versions.md) controlli comuni, le barre degli strumenti ignorano il flag [**\_ CDRF NEWFONT.**](cdrf-constants.md) La versione 6.0 supporta il flag **CDRF \_ NEWFONT** ed è possibile usarlo per selezionare un tipo di carattere diverso per la barra degli strumenti. Tuttavia, non è possibile modificare il colore di una barra degli strumenti quando è attivo uno stile di visualizzazione. Per modificare il colore di una barra degli strumenti nella versione 6.0, è prima necessario disabilitare gli stili di visualizzazione chiamando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) e senza specificare alcuno stile di visualizzazione:

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Disegno personalizzato con List-View e Tree-View personalizzati

I controlli più comuni possono essere gestiti essenzialmente nello stesso modo. Tuttavia, i controlli visualizzazione elenco e visualizzazione albero hanno alcune funzionalità che richiedono un approccio leggermente diverso al disegno personalizzato.

Per [la versione 5.0,](common-control-versions.md)questi due controlli possono visualizzare testo ritagliato se si modifica il tipo di carattere tramite la restituzione di [**CDRF \_ NEWFONT**](cdrf-constants.md). Questo comportamento è necessario per la compatibilità con le versioni precedenti dei controlli comuni. Se si vuole modificare il tipo di carattere di un controllo visualizzazione elenco o visualizzazione albero, si otterrà risultati migliori se si invia un messaggio [**CCM \_ SETVERSION**](ccm-setversion.md) con il valore *wParam* impostato su 5 prima di aggiungere elementi al controllo. Per un esempio di un controllo visualizzazione albero che usa il disegno personalizzato Knowledge Base, vedere l'articolo [SAMPLE: CustDTv Illustra il disegno personalizzato in un controllo TreeView (Q248496).]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)

### <a name="custom-draw-with-list-view-controls"></a>Disegno personalizzato con List-View personalizzati

Poiché i controlli visualizzazione elenco hanno elementi secondari e più modalità di visualizzazione, sarà necessario gestire la notifica [ \_ NM CUSTOMDRAW](nm-customdraw.md) in modo leggermente diverso rispetto agli altri controlli comuni.

Per la modalità report, usare la procedura seguente.

1.  La prima [notifica DI NM \_ CUSTOMDRAW](nm-customdraw.md) avrà il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata impostata su CDDS \_ PREPAINT. Restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Si riceverà quindi una [notifica DI NM \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT. Se si specificano nuovi tipi di carattere o colori e si restituisce [**CDRF \_ NEWFONT,**](cdrf-constants.md)tutti gli elementi secondari dell'elemento verranno modificati. Se invece si vuole gestire separatamente ogni elemento secondario, restituire [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md).
3.  Se è stato [**restituito CDRF \_ NOTIFYSUBITEMDRAW nel**](cdrf-constants.md) passaggio precedente, si riceverà una notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) per ogni elemento secondario con **dwDrawStage** impostato su CDDS \_ SUBITEM \| CDDS \_ ITEMPREPAINT. Per modificare il tipo di carattere o il colore per l'elemento secondario, specificare un nuovo tipo di carattere o colore e restituire [**CDRF \_ NEWFONT**](cdrf-constants.md).

Per le modalità icona grande, icona piccola ed elenco, seguire questa procedura.

1.  La prima [notifica DI NM \_ CUSTOMDRAW](nm-customdraw.md) avrà il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata impostata su CDDS \_ PREPAINT. Restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Si riceverà quindi una [notifica DI NM \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT. È possibile modificare i tipi di carattere o i colori di un elemento specificando nuovi tipi di carattere e colori e restituisce [**CDRF \_ NEWFONT**](cdrf-constants.md). Poiché queste modalità non hanno elementi secondari, non si riceveranno altre notifiche DI NM \_ CUSTOMDRAW.

Per un esempio di un gestore di notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) per la visualizzazione elenco, vedere [Using Custom Draw](using-custom-draw.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso del disegno personalizzato](using-custom-draw.md)
</dt> <dt>

[Informazioni di riferimento sul disegno personalizzato](custom-draw-reference.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[ESEMPIO: CustDTv illustra il disegno personalizzato in un controllo TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 