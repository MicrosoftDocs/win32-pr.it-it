---
title: Elementi recenti
description: L'elenco degli elementi recenti è un riquadro del menu dell'applicazione in cui vengono visualizzati gli elementi utilizzati più di recente per un'applicazione.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555949"
---
# <a name="recent-items"></a>Elementi recenti

L'elenco degli elementi recenti è un riquadro del [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) in cui vengono visualizzati gli elementi utilizzati più di recente per un'applicazione.

-   [Dettagli](#details)
-   [Proprietà degli elementi recenti](#recent-items-properties)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Lo screenshot seguente illustra un elenco di elementi recenti da WordPad per Windows 7.

![screenshot dell'elenco di elementi recenti nella barra multifunzione di Microsoft Paint.](images/controls/recentitems.png)

Il [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) può contenere al massimo un elenco [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , rappresentato da un elemento **ApplicationMenu. RecentItems** , per la visualizzazione di documenti recenti, immagini, filmati e altri progetti su cui un utente sta lavorando. Il numero di elementi elencati è compreso tra 0 e il numero massimo specificato nel markup e il valore predefinito è dieci. Gli elementi recenti vengono visualizzati come un elenco numerato di stringhe che indicano i nomi di file. È consigliabile usare la proprietà [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) per fornire il percorso completo per il percorso del file, come illustrato nella schermata seguente.

![Screenshot di un elenco di elementi recenti nel menu di un'applicazione.](images/overviews/applicationmenu-menurecentitems.png)

L'elemento [**RecentItems**](windowsribbon-element-recentitems.md) ha un attributo *EnablePinning* che, se impostato su `true` , Visualizza un'icona a forma di puntina a destra di ogni elemento nell'elenco, come illustrato nella schermata seguente.

> [!Note]  
> Il blocco è abilitato per impostazione predefinita se l'attributo *EnablePinning* non è specificato.

 

![screenshot dell'aggiunta di elementi recenti nel menu di un'applicazione.](images/overviews/applicationmenu-menurecentitemspinned.png)

L'algoritmo di blocco ha lo scopo di evitare che gli elementi cadano nell'elenco **degli elementi recenti** . L'algoritmo produce il comportamento seguente:

-   Un nuovo elemento viene sempre aggiunto all'inizio dell'elenco di **elementi recenti** .
-   Gli elementi vengono spostati nell'elenco nel tempo. Quando l'elenco è pieno (raggiunge il numero massimo di elementi specificato nel markup), gli elementi meno recenti rientrano nella parte inferiore dell'elenco man volta che vengono aggiunti nuovi elementi all'inizio dell'elenco.
-   Se un elemento è già presente nell'elenco, ma viene nuovamente eseguito l'accesso, viene spostato di nuovo nella parte superiore dell'elenco.
-   Se un elemento è bloccato, verrà comunque spostata verso il basso nell'elenco, ma non verrà escluso. Al contrario, una volta completato l'elenco, il primo elemento rimosso sopra l'elemento bloccato verrà disattivato quando viene aggiunto un nuovo elemento all'elenco.
-   Se il numero di elementi bloccati raggiunge il numero massimo di elementi, nessun nuovo elemento verrà aggiunto all'elenco fino a quando non viene sbloccato un elemento.

## <a name="recent-items-properties"></a>Proprietà degli elementi recenti

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo degli elementi recenti.

In genere, una proprietà degli elementi recenti viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo elementi recenti.



| Chiave della proprietà                                                                       | Note                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)           | Può essere aggiornato solo tramite l'invalidamento. |
| [Interfaccia utente \_ pkey \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md) | Può essere aggiornato solo tramite l'invalidamento. |



 

## <a name="remarks"></a>Commenti

Il metodo [IApplicationDocumentLists:: GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) può essere usato per recuperare l'elenco di Windows Shell MRU per l'applicazione Ribbon. L'oggetto recuperato da questo metodo può quindi essere utilizzato dall'applicazione per creare i dati richiesti dal framework della barra multifunzione per popolare l'elenco di **elementi recenti** del [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).

> [!Note]  
> Quando si usa questo metodo, *ListType* deve avere il valore `ADLT_RECENT` .

 

Per un esempio di come implementare un elenco di elementi MRU in un'applicazione di Framework della barra multifunzione, vedere l' [esempio HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup elementi recenti**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 