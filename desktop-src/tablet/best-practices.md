---
description: Panoramica delle procedure consigliate per l'uso dell'oggetto pannello input penna.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Procedure consigliate (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234084"
---
# <a name="best-practices-tablet-pc"></a>Procedure consigliate (Tablet PC)

Esistono alcune linee guida da tenere presenti quando si usa l'oggetto [**PenInputPanel**](peninputpanel-class.md) .

-   [Preferisci controllo InkEdit](#prefer-inkedit-control)
-   [Disabilitare la modalità input penna nei controlli InkEdit](#disable-ink-mode-on-inkedit-controls)
-   [Uso di controlli senza finestra](#using-windowless-controls)
-   [Argomenti correlati](#related-topics)

## <a name="prefer-inkedit-control"></a>Preferisci controllo InkEdit

[InkEdit](inkedit-control-reference.md) è il controllo preferito a cui alleghi l'oggetto [**PenInputPanel**](peninputpanel-class.md) . Il controllo InkEdit fornisce il supporto per il [Framework dei servizi di testo (TSF)](text-services-framework.md).

## <a name="disable-ink-mode-on-inkedit-controls"></a>Disabilitare la modalità input penna nei controlli InkEdit

Quando viene collegato a un controllo [InkEdit](inkedit-control-reference.md) , impostare la proprietà [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del controllo InkEdit sul valore [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) . Se la proprietà **InkMode** non è impostata sul valore **InkMode** , il controllo InkEdit interpreta il primo tap come tratto, lo passa al riconoscimento e inserisce il testo nel controllo InkEdit. Poiché si dispone già di un oggetto [**PenInputPanel**](peninputpanel-class.md) collegato per accettare input penna, non è necessario che il controllo InkEdit sia abilitato anche per l'input penna.

## <a name="using-windowless-controls"></a>Uso di controlli senza finestra

Quando un oggetto [**PenInputPanel**](peninputpanel-class.md) è associato a una finestra padre che contiene più di un controllo senza finestra, l'oggetto **PenInputPanel** non sa come tenere traccia del punto di inserimento quando lo stato attivo viene spostato tra gli elementi figlio senza finestra. L'input della grafia può essere inviato al figlio errato quando lo stato attivo viene spostato da un controllo senza finestra a un altro mentre l'input è in sospeso.

Per usare l'oggetto [**PenInputPanel**](peninputpanel-class.md) in un ambiente privo di finestra, è possibile usare la tecnica seguente:

1.  Crea un'istanza di un controllo [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) e la posiziona sul controllo senza finestra.
2.  Alleghi l'oggetto [**PenInputPanel**](peninputpanel-class.md) al nuovo controllo casella di testo.
3.  Consentire al controllo casella di testo di raccogliere il testo riconosciuto dall'oggetto [**PenInputPanel**](peninputpanel-class.md) .
4.  Quando lo stato attivo si sposta dal controllo casella di testo, chiamare il metodo [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) dell'oggetto [**PenInputPanel**](peninputpanel-class.md) .
5.  Copiare il testo riconosciuto dal controllo casella di testo nell'elemento figlio privo di finestra.
6.  Scollegare l'oggetto [**PenInputPanel**](peninputpanel-class.md) impostando la proprietà [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo codice gestito) o la proprietà [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) su null.
7.  Elimina il controllo casella di testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe PenInputPanel**](peninputpanel-class.md)
</dt> <dt>

[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Text Services Framework](../tsf/text-services-framework.md)
</dt> </dl>

 

 
