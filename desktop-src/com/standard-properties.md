---
title: Proprietà standard
description: Proprietà standard
ms.assetid: 08b7c388-a362-4d71-ac24-93675984881f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ab30dd644231c5c11a9f1e4d7ccf9c861ae2fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047397"
---
# <a name="standard-properties"></a>Proprietà standard

OLE definisce un set di DISPID standard per tutti e tre i tipi di proprietà: Control, ambient ed Extended. Nelle tabelle seguenti sono elencati questi standard per le proprietà del controllo, le proprietà di ambiente e le proprietà estese.



| Proprietà del controllo                                                                               | Tipo                             | Descrizione                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor, FillColor, BorderColor<br/>                                        | **\_colore OLE**<br/>        | Combinazione colori del controllo<br/>                                                                                                                                                                                                    |
| BackStyle, FillStyle, BorderStyle, BorderWidth, BorderVisible, DrawStyle, DrawWidth<br/> | **short** o **Long**<br/> | Bit che definiscono il comportamento visivo di un controllo, ad esempio una tinta unita o trasparente, con bordi spessi o sottili, stili di linea e così via.<br/>                                                                                    |
| Carattere<br/>                                                                                | **IDispatch \***<br/>      | Il tipo di carattere utilizzato nel controllo, che è un puntatore **IDispatch** a un oggetto tipo di carattere standard. Per ulteriori informazioni, vedere [oggetto tipo di carattere standard](standard-font-object.md) .<br/>                                                         |
| Didascalia, testo<br/>                                                                       | **BSTR**<br/>              | Stringhe contenenti l'etichetta del controllo (la didascalia) o il relativo contenuto testuale (il testo). Si noti che la didascalia non indica necessariamente il nome del controllo nel contenitore. Vedere la proprietà nome esteso nella tabella seguente.<br/> |
| Abilitato<br/>                                                                             | **BOOL**<br/>              | Determina se il controllo è abilitato o disabilitato. Se disabilitato, il controllo è probabilmente grigio.<br/>                                                                                                                           |
| Finestra<br/>                                                                              | **HWND**<br/>              | Handle della finestra del controllo, se ne è presente uno.<br/>                                                                                                                                                                              |
| TabStop<br/>                                                                             | **BOOL**<br/>              | Determina se questo controllo è una tabulazione.<br/>                                                                                                                                                                                |



 



| Proprietà di ambiente                         | Tipo                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor<br/>          | **\_colore OLE**<br/>   | Fornisce controlli con i colori di sfondo e di primo piano predefiniti. L'utilizzo da un controllo è facoltativo.<br/>                                                                                                                                                                                                                                                                                          |
| Carattere<br/>                          | **IDispatch \***<br/> | Puntatore a un oggetto tipo di carattere standard che definisce il tipo di carattere predefinito per il form. L'utilizzo da un controllo è facoltativo. Per ulteriori informazioni, vedere [oggetto tipo di carattere standard](standard-font-object.md) .<br/>                                                                                                                                                                                                    |
| LocaleID<br/>                      | **LCID**<br/>         | Lingua utilizzata nel contenitore. L'uso da un controllo è consigliato.<br/>                                                                                                                                                                                                                                                                                                                        |
| UserMode<br/>                      | **BOOL**<br/>         | Descrive se il contenitore è in modalità progettazione (**false**) o in modalità di esecuzione (**true**), che deve essere utilizzato da un controllo per modificare le funzionalità disponibili in base alle esigenze.<br/>                                                                                                                                                                                                                      |
| UIDead<br/>                        | **BOOL**<br/>         | Descrive se il contenitore si trova in una modalità in cui i controlli devono ignorare l'input dell'utente. Si applica indipendentemente da UserMode. Un contenitore può sempre impostare UIDead su **true** in modalità progettazione e può impostarlo su **true** quando ha raggiunto un punto di interruzione o tale durante la modalità di esecuzione. Un controllo deve prestare attenzione a questa proprietà.<br/>                                                                |
| MessageReflect<br/>                | **BOOL**<br/>         | Specifica se il contenitore desidera ricevere messaggi di Windows, ad esempio WM \_ CTLCOLOR, WM \_ DrawItem, WM \_ PARENTNOTIFY e così via, come eventi.<br/>                                                                                                                                                                                                                                           |
| SupportsMnemonics<br/>             | **BOOL**<br/>         | Descrive se il contenitore elabora i tasti di scelta. Un controllo può eseguire tutte le operazioni desiderate con queste informazioni, ad esempio caratteri non sottolineati, che in genere viene utilizzato come tasto di scelta.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles, ShowHatching<br/> | **BOOL**<br/>         | Descrive se un controllo deve mostrare un bordo del tratteggio o i punti di controllo (nel bordo del tratteggio) quando sono attivi sul posto. I controlli devono rispettare queste proprietà, offrendo al contenitore il controllo finale sugli utenti che disegnano effettivamente questi bit dell'interfaccia utente. È possibile che un contenitore di controlli desideri definirne uno proprio anziché affidarsi a ogni controllo, nel qual caso questi ambienti sono sempre **false**.<br/> |
| DisplayAsDefault<br/>              | **BOOL**<br/>         | Il contenitore esporrà un **true** per questa proprietà tramite il sito che contiene ciò che è contrassegnato come pulsante predefinito quando il controllo Button deve disegnarsi con un frame predefinito più spessa.<br/>                                                                                                                                                                                         |



 



| Proprietà estesa          | Tipo                        | Descrizione                                                           |
|----------------------------|-----------------------------|-----------------------------------------------------------------------|
| Nome<br/>            | **BSTR**<br/>         | Nome del contenitore per il controllo.<br/>                      |
| Visible<br/>         | **BOOL**<br/>         | Visibilità del controllo.<br/>                                  |
| Padre<br/>          | **IDispatch \***<br/> | Interfaccia dispatch del form che contiene il controllo.<br/>      |
| Impostazione predefinita, Annulla<br/> | **BOOL**<br/>         | Indica se il controllo è il pulsante predefinito o Annulla.<br/> |



 

Tutte queste proprietà standard hanno valori DISPID negativi, che ne indicano lo stato standard.

Si noti che, per evitare conflitti nei simboli a livello di codice per questi DISPID, a tutte le proprietà di ambiente vengono assegnati simboli nella proprietà di ambiente DISPID di form \_ \_  come in \_ ambiente DISPID \_ . Tutti gli altri simboli utilizzano \_ la *Proprietà* DISPID come di consueto.

Alcune proprietà di ambiente, nonché le proprietà dei controlli, coinvolgono i colori. Il tipo di **\_ colore OLE** indicato nelle tabelle precedenti può fare riferimento a un tipo **COLORREF** standard, un indice a una tavolozza, un indice relativo della tavolozza o un indice dei colori di sistema usato con la funzione [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) . La funzione [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor) converte un tipo di **\_ colore OLE** in un tipo **COLORREF** in base a una tavolozza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo](control-properties.md)
</dt> </dl>

 

