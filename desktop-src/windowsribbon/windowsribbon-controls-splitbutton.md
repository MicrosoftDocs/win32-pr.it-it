---
title: Pulsante di menu combinato
description: Il pulsante di suddivisione è un controllo composito con il quale l'utente può selezionare un valore predefinito associato a un pulsante primario oppure selezionare da un elenco di valori che si escludono a vicenda, visualizzati in un elenco a discesa associato a un pulsante secondario.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300592"
---
# <a name="split-button"></a>Pulsante di menu combinato

Il pulsante di suddivisione è un controllo composito con il quale l'utente può selezionare un valore predefinito associato a un pulsante primario oppure selezionare da un elenco di valori che si escludono a vicenda, visualizzati in un elenco a discesa associato a un pulsante secondario.

-   [Introduzione](#introduction)
-   [Proprietà pulsante di divisione](#split-button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Questo controllo è utile per esporre elementi strettamente correlati nei casi in cui è disponibile un valore predefinito ovvio e in cui i singoli elementi possono essere rappresentati da un'immagine, un testo o entrambi.

Lo screenshot seguente illustra il pulsante di suddivisione della barra multifunzione.

![Screenshot di un controllo SplitButton in una barra multifunzione di esempio.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Proprietà pulsante di divisione

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo pulsante di divisione.

In genere, la proprietà di un pulsante di suddivisione viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo pulsante di divisione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Chiave della proprietà</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.<br/> Se tutti gli elementi figlio sono disabilitati, il Framework imposta <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> su false (0). In caso contrario, se sono abilitati uno o più elementi figlio, UI_PKEY_Enabled viene impostato su true (-1).
<blockquote>
[!Important]<br />
Quando uno o più elementi figlio sono abilitati o disabilitati, la proprietà <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> per il controllo pulsante di suddivisione deve essere invalidata. In questo modo il Framework esegue una query sul valore della proprietà aggiornata e aggiorna lo stato del controllo pulsante di suddivisione nell'interfaccia utente della barra multifunzione.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>