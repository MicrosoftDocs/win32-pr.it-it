---
title: Menu applicazione
description: Il menu dell'applicazione è il menu principale di un'applicazione che implementa il Framework della barra multifunzione di Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872537"
---
# <a name="application-menu"></a>Menu applicazione

Il menu dell'applicazione è il menu principale di un'applicazione che implementa il Framework della barra multifunzione di Windows.

-   [Introduzione](#introduction)
-   [Componenti del menu dell'applicazione](#components-of-the-application-menu)
    -   [Menu dell'applicazione MenuGroup](#application-menu-menugroup)
-   [Ridimensionamento del menu dell'applicazione](#sizing-the-application-menu)
-   [Proprietà del menu applicazione](#application-menu-properties)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il menu applicazione è costituito da un controllo pulsante a discesa che consente di visualizzare un menu che contiene i comandi che espongono le funzionalità correlate a un progetto completo, ad esempio un intero documento, un'immagine o un film. Gli esempi includono i comandi **nuovi**, **Apri**, **Salva** ed **Esci** .

Lo screenshot seguente illustra il menu dell'applicazione.

![screenshot del menu dell'applicazione e dell'elenco di elementi recenti della barra multifunzione di Paint per Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a>Componenti del menu dell'applicazione

Il menu dell'applicazione è un elemento obbligatorio in qualsiasi applicazione della barra multifunzione. Il punto di ingresso nel menu dell'applicazione è un pulsante distinto visualizzato come primo elemento nella riga di [tabulazione](windowsribbon-controls-tab.md) , come illustrato nella schermata seguente.

> [!Note]  
> Windows 8 e versioni successive: l'immagine del pulsante di menu dell'applicazione è cambiata in etichetta: **file**. Si consiglia di non usare file come etichetta per le schede.

 

![screenshot del pulsante di menu dell'applicazione di WordPad per Windows 7.](images/overviews/applicationmenu-button.png)

Quando si fa clic su questo pulsante, viene visualizzato il menu completo visualizzato nello screenshot seguente (il menu dell'applicazione da WordPad per Windows 7).

![screenshot del menu di menu dell'applicazione di WordPad per Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> Non vi è alcun effetto sul set di schede quando si fa clic sul pulsante di menu dell'applicazione; lo stato attivo entra invece nel menu.

 

Il menu dell'applicazione contiene due riquadri: un elenco di comandi rappresentati da uno o più elementi [**MenuGroup**](windowsribbon-element-menugroup.md) e un elenco di [elementi recenti](windowsribbon-controls-recentitems.md) rappresentato da un elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .

### <a name="application-menu-menugroup"></a>Menu dell'applicazione MenuGroup

L'elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) deve contenere almeno un elemento figlio [**MenuGroup**](windowsribbon-element-menugroup.md) che espone un elenco di comandi a livello di applicazione. Se vengono dichiarati più elementi **MenuGroup** , viene disegnata una linea di divisione tra i gruppi, come illustrato nella schermata seguente.

![screenshot del menu di un'applicazione MenuGroup.](images/overviews/applicationmenu-menugroup.png)

Di seguito è riportato un elenco di vincoli per un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) di un menu dell'applicazione:

-   Tutti gli elementi [**MenuGroup**](windowsribbon-element-menugroup.md) devono essere dichiarati con un valore dell'attributo della *classe* `MajorItems` .
-   Un menu applicazione  [**MenuGroup**](windowsribbon-element-menugroup.md) supporta solo i controlli [pulsante](windowsribbon-controls-button.md), [interruttore](windowsribbon-controls-togglebutton.md), pulsante a [discesa](windowsribbon-controls-dropdownbutton.md), pulsante di menu [combinato](windowsribbon-controls-splitbutton.md), [raccolta a discesa](windowsribbon-controls-dropdowngallery.md)e [raccolta pulsanti](windowsribbon-controls-splitbuttongallery.md) di menu combinato.
    > \[! Importante\]  
    > Le raccolte di comandi sono l'unico tipo di raccolta supportato nel menu dell'applicazione. Per altre informazioni sui controlli della raccolta, vedere [uso delle raccolte](./ribbon-controls-galleries.md).

     

Quando si usa un [pulsante](windowsribbon-controls-button.md) o un [interruttore](windowsribbon-controls-togglebutton.md) in un [**MenuGroup**](windowsribbon-element-menugroup.md), il valore di [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) viene visualizzato nel menu e i valori di [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) e [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) vengono visualizzati come descrizione comando, come illustrato nella schermata seguente.

![Screenshot di un controllo Button nel menu di un'applicazione.](images/overviews/applicationmenu-menubutton.png)

Quando si usa un [pulsante a discesa](windowsribbon-controls-dropdownbutton.md), un pulsante di menu [combinato](windowsribbon-controls-splitbutton.md), una raccolta a [discesa](windowsribbon-controls-dropdowngallery.md)o una raccolta di pulsanti di menu [combinato](windowsribbon-controls-splitbuttongallery.md) , la parte di menu viene visualizzata come un riquadro a comparsa che copre e nasconde il riquadro **elementi recenti** .

Per i controlli pulsante di menu [combinato](windowsribbon-controls-splitbutton.md) e [pulsante a discesa](windowsribbon-controls-dropdownbutton.md) , il valore di [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) viene visualizzato inline nel menu a comparsa per aiutare gli utenti a individuare la funzionalità del comando. Il valore visualizzato di **Command. LabelDescription** viene suddiviso a livello di codice su un intervallo a due righe e viene effettuato un tentativo di adattare il valore esattamente sul riquadro **elementi recenti** sotto. Se il valore **Command. LabelDescription** non è adatto, il riquadro a comparsa si espanderà in modo da includere il valore più lungo del [**comando. Comment**](windowsribbon-element-command-comment.md) in [**MenuGroup**](windowsribbon-element-menugroup.md).

Lo screenshot seguente illustra questi comportamenti in un riquadro a comparsa di un [pulsante di menu combinato](windowsribbon-controls-splitbutton.md) .

![Screenshot di un riquadro a comparsa di un controllo elenco nel menu di un'applicazione.](images/overviews/applicationmenu-menuflyout.png)

Con una raccolta a [discesa](windowsribbon-controls-dropdowngallery.md) e una [raccolta di pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md), vengono visualizzate solo un'etichetta e un'immagine.

## <a name="sizing-the-application-menu"></a>Ridimensionamento del menu dell'applicazione

Il dimensionamento del menu applicazione è gestito dal framework della barra multifunzione. Se vengono fornite stringhe molto lunghe per il valore di [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md)oppure viene utilizzato un lungo elenco di comandi, il menu ne modificherà le dimensioni per adattarlo al contenuto. Alcune forme di regolazione includono l'espansione delle dimensioni dei riquadri riquadri a comparsa o menu e l'aggiunta di visualizzatori di Pan quando è necessario lo scorrimento.

## <a name="application-menu-properties"></a>Proprietà del menu applicazione

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo menu applicazione.

In genere, una proprietà del menu applicazione viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà vengono definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e per l'applicazione non viene eseguita una query per ottenere un valore di proprietà aggiornato fino a quando la proprietà non è richiesta dal Framework. Il Framework, ad esempio, richiede la proprietà quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.



| Chiave della proprietà                                                                                     | Note                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Interfaccia utente \_ pkey \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite l'invalidamento. |
| [Interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite l'invalidamento. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup ApplicationMenu**](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 