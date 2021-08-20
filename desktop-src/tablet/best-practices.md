---
description: Panoramica delle procedure consigliate quando si usa l'oggetto pannello di input penna.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Procedure consigliate (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a08235923d4db49d1b5960a37ba956465219aeb7865b89f653f8d731b86b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046158"
---
# <a name="best-practices-tablet-pc"></a>Procedure consigliate (Tablet PC)

Quando si usa l'oggetto [**PenInputPanel,**](peninputpanel-class.md) è necessario tenere presenti alcune linee guida.

-   [Preferire il controllo InkEdit](#prefer-inkedit-control)
-   [Disabilitare la modalità input penna nei controlli InkEdit](#disable-ink-mode-on-inkedit-controls)
-   [Uso di controlli senza finestra](#using-windowless-controls)
-   [Argomenti correlati](#related-topics)

## <a name="prefer-inkedit-control"></a>Preferire il controllo InkEdit

[InkEdit](inkedit-control-reference.md) è il controllo preferito a cui associare [**l'oggetto PenInputPanel.**](peninputpanel-class.md) Il controllo InkEdit fornisce il supporto per [Framework servizi di testo (TSF).](text-services-framework.md)

## <a name="disable-ink-mode-on-inkedit-controls"></a>Disabilitare la modalità input penna nei controlli InkEdit

Quando è associato a un [controllo InkEdit,](inkedit-control-reference.md) impostare la [**proprietà InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del controllo InkEdit sul [**valore InkMode.**](/windows/desktop/api/inked/ne-inked-inkmode) Se la proprietà **InkMode** non è impostata sul valore **InkMode,** il controllo InkEdit interpreta il primo tocco come tratto, lo passa al sistema di riconoscimento e inserisce il testo nel controllo InkEdit. Poiché è già presente un [**oggetto PenInputPanel**](peninputpanel-class.md) associato per accettare l'input penna, non è necessario che il controllo InkEdit sia abilitato anche per l'input penna.

## <a name="using-windowless-controls"></a>Uso di controlli senza finestra

Quando un [**oggetto PenInputPanel**](peninputpanel-class.md) è associato a una finestra padre che contiene più di un controllo senza finestra, l'oggetto **PenInputPanel** non sa come tenere traccia del cursore quando lo stato attivo si sposta tra gli elementi figlio senza finestra. L'input di scrittura manuale può essere inviato all'elemento figlio errato quando lo stato attivo passa da un controllo senza finestra a un altro mentre l'input è in sospeso.

Per usare [**l'oggetto PenInputPanel**](peninputpanel-class.md) in un ambiente senza finestra, è possibile usare la tecnica seguente:

1.  Creare [un'istanza di un](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) controllo TextBox e posizionarlo sul controllo senza finestra.
2.  Associare [**l'oggetto PenInputPanel**](peninputpanel-class.md) al nuovo controllo casella di testo.
3.  Consentire al controllo casella di testo di raccogliere il testo riconosciuto [**dall'oggetto PenInputPanel.**](peninputpanel-class.md)
4.  Quando lo stato attivo viene rimosso dal controllo casella di testo, chiamare il [**metodo CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) dell'oggetto [**PenInputPanel.**](peninputpanel-class.md)
5.  Copiare il testo riconosciuto dal controllo casella di testo all'elemento figlio senza finestra.
6.  Scollegare [**l'oggetto PenInputPanel**](peninputpanel-class.md) impostandone la proprietà [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo codice gestito) o [**La proprietà AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) su Null.
7.  Eliminare il controllo casella di testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe PenInputPanel**](peninputpanel-class.md)
</dt> <dt>

[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Text Services Framework](../tsf/text-services-framework.md)
</dt> </dl>

 

 
