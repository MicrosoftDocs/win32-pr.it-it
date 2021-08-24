---
title: Elementi recenti
description: L'elenco Elementi recenti è un riquadro del menu dell'applicazione che visualizza gli elementi usati più di recente per un'applicazione.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1d67c38e1eb9014cfd3349881ed2849755ebc89489cc925052aa690f54adc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810883"
---
# <a name="recent-items"></a>Elementi recenti

L'elenco Elementi recenti è un riquadro del [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) che visualizza gli elementi usati più di recente per un'applicazione.

-   [Dettagli](#details)
-   [Proprietà degli elementi recenti](#recent-items-properties)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Lo screenshot seguente illustra un elenco Elementi recenti da WordPad per Windows 7).

![screenshot dell'elenco di elementi recenti nella barra multifunzione di Microsoft Paint.](images/controls/recentitems.png)

Il [menu](windowsribbon-controls-applicationmenu.md) dell'applicazione può avere al massimo un elenco [**ApplicationMenu.RecentItems,**](windowsribbon-element-applicationmenu-recentitems.md) rappresentato da un elemento **ApplicationMenu.RecentItems,** per visualizzare documenti, immagini, film e altri progetti recenti su cui un utente ha lavorato. Il numero di elementi elencati è compreso tra zero e il numero massimo specificato nel markup, con un valore predefinito di dieci. Gli elementi recenti vengono visualizzati come elenco numerato di stringhe che indicano i nomi di file. È consigliabile usare la [**proprietà Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) per fornire il percorso completo per il percorso del file, come illustrato nello screenshot seguente.

![screenshot di un elenco di elementi recenti in un menu dell'applicazione.](images/overviews/applicationmenu-menurecentitems.png)

[**L'elemento RecentItems**](windowsribbon-element-recentitems.md) ha un attributo *EnablePinning* che, se impostato su , visualizza un'icona a forma di puntina a destra di ogni elemento nell'elenco, come illustrato nello `true` screenshot seguente.

> [!Note]  
> L'aggiunta è abilitata per impostazione predefinita se *l'attributo EnablePinning* non è specificato.

 

![screenshot degli elementi recenti che si bloccano nel menu di un'applicazione.](images/overviews/applicationmenu-menurecentitemspinned.png)

L'algoritmo di blocco è progettato per evitare che gli elementi esegnino **dall'elenco Elementi** recenti . L'algoritmo produce il comportamento seguente:

-   Un nuovo elemento viene sempre aggiunto all'inizio **dell'elenco Elementi** recenti .
-   Gli elementi verranno spostati verso il basso nell'elenco nel tempo. Quando l'elenco è pieno (raggiunge il numero massimo di elementi specificato nel markup), gli elementi meno recenti vengono eliminati dalla parte inferiore dell'elenco quando vengono aggiunti nuovi elementi all'inizio dell'elenco.
-   Se un elemento è già presente in un punto dell'elenco, ma vi si accede nuovamente, torna all'inizio dell'elenco.
-   Se un elemento viene aggiunto, continuerà a essere visualizzato verso il basso nell'elenco, ma non cadrà nella parte inferiore. Al contrario, quando l'elenco è pieno, il primo elemento non bloccato sopra l'elemento aggiunto viene disattivato quando viene aggiunto un nuovo elemento all'elenco.
-   Se il numero di elementi aggiunti raggiunge il numero massimo di elementi, non verranno aggiunti nuovi elementi all'elenco finché non viene sbloccato un elemento.

## <a name="recent-items-properties"></a>Proprietà degli elementi recenti

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Elementi recenti.

In genere, una proprietà Elementi recenti viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al [**metodo IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidamento viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Elementi recenti.



| Chiave di proprietà                                                                       | Note                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Suggerimento \_ tasto di scelta \_ PKEY dell'interfaccia utente](windowsribbon-reference-properties-uipkey-keytip.md)           | Può essere aggiornato solo tramite invalidamento. |
| [UI \_ PKEY \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md) | Può essere aggiornato solo tramite invalidamento. |



 

## <a name="remarks"></a>Commenti

Il [metodo IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) può essere usato per recuperare l Windows MRU della shell per l'applicazione della barra multifunzione. L'oggetto recuperato da questo metodo può quindi essere usato dall'applicazione per creare  i dati richiesti dal framework della barra multifunzione per popolare l'elenco Elementi recenti del [menu dell'applicazione.](windowsribbon-controls-applicationmenu.md)

> [!Note]  
> Quando si usa questo metodo, *listtype* deve avere il valore `ADLT_RECENT` .

 

Per un esempio di come implementare un elenco di elementi MRU in un'applicazione framework della barra multifunzione, vedere [l'esempio HTMLEditRibbon.](windowsribbon-htmleditribbonsample.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli del framework della barra multifunzione](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup Recent Items**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 