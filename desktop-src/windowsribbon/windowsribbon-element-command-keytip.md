---
title: Proprietà Command. suggerimento
description: Rappresenta il suggerimento tasto di ricerca per un controllo.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Barra multifunzione di Windows della proprietà Command. suggerimento
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302317"
---
# <a name="commandkeytip-property"></a>Proprietà Command. suggerimento

Rappresenta il suggerimento tasto di ricerca per un controllo.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Descrizione                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Stringa**](windowsribbon-element-string.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni elemento [**Command**](windowsribbon-element-command.md) .

**Command. suggerimento. suggerimento** può contenere un valore di tipo *xs: String* vincolato a qualsiasi sequenza di caratteri Unicode, incluso lo spazio vuoto.

Un **comando. suggerimento suggerimento** può iniziare con un numero solo se associato a un controllo all'interno di una [scheda](windowsribbon-controls-tab.md) o della [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md).

Per visualizzare i suggerimenti tasti validi per lo stato corrente della barra multifunzione, tenere premuto ALT. Lo screenshot seguente mostra i suggerimenti di tasti iniziali, o di primo livello, visualizzati in Microsoft Paint per Windows 7. Dopo aver selezionato un suggerimento tasto di scelta di primo livello, vengono visualizzati solo i suggerimenti tasti di secondo livello.

![suggerimenti dei tasti di primo livello in Microsoft Paint per Windows 7](images/properties/ui-pkey-label-keytips.png)

**Command.** hotkey funge da tasto di scelta rapida per un comando, a meno che il comando non venga esposto tramite una voce di menu. In questo caso, il Framework ignora il valore **Command. suggerimento** e usa invece un carattere preceduto da una e commerciale come specificato da [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [dall' \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md). Se nessuna e commerciale è specificata da **Command. LabelTitle** o dall'etichetta pkey dell'interfaccia utente \_ \_ , non viene esposto alcun tasto di scelta rapida o tasto di scelta rapida.

Se non viene specificato alcun valore per **Command. suggerimento**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.

> [!Note]  
> Se **Command. textsuggerimento** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.

 

Per impostazione predefinita, le lettere seguenti vengono usate dal Framework per generare automaticamente i suggerimenti dei tasti:

-   **F** viene assegnato al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).
-   **Y** viene assegnato a qualsiasi comando che non dispone di un tasto di suggerimento specificato dall'applicazione.
-   La **Z** viene assegnata a ogni controllo del [gruppo](windowsribbon-controls-group.md) e non può essere personalizzata. Un suggerimento tasto di gruppo viene visualizzato solo quando [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) per il controllo specifica un'opzione di dimensioni **popup** . Per ulteriori informazioni, vedere [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).

> [!Note]  
> Nessuna di queste lettere è riservata dal Framework. Ogni può essere assegnato a uno o più comandi in modo obbligatorio.

 

Il Framework risolve i conflitti del tasto di suggerimento nei modi seguenti:

-   Se uno o più controlli struttura a schede sono associati allo stesso suggerimento tasto di aggiunta, viene aggiunto un numero a ogni suggerimento [tasto](windowsribbon-controls-tab.md) di ricerca, a partire da 1 e aumentando in sequenza (2, 3,...) per ogni controllo nell'ordine di dichiarazione. Se ai controlli a schede viene assegnata la lettera F come suggerimento tasto di scelta, al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) viene assegnato F1 con i suggerimenti di tasti rimanenti, come descritto.
-   Quando è associato a un singolo controllo all'interno di una [scheda](windowsribbon-controls-tab.md), il suggerimento tasto F è valido sia per il controllo che per il [menu applicazione](windowsribbon-controls-applicationmenu.md). Il tasto di scelta rapida del menu applicazione predefinito non viene modificato, ma la precedenza viene assegnata al controllo nella scheda attiva.
-   Se uno o più controlli all'interno di una scheda sono associati allo stesso [tasto](windowsribbon-controls-tab.md) di suggerimento, il Framework esegue automaticamente il refactoring dei suggerimenti di questi controlli, come descritto in precedenza.

> [!Note]  
> Una lieve variazione del colore del testo viene usata per evidenziare i suggerimenti per i tasti di refactoring in un'implementazione standard della barra multifunzione. Per un'implementazione della barra multifunzione non standard in cui il colore della barra multifunzione è stato personalizzato, viene eseguito l'override di questo comportamento del Framework e vengono visualizzati tutti i suggerimenti dei tasti con lo stesso colore del testo. Per ulteriori informazioni, vedere [personalizzazione dei colori della barra multifunzione](ribbon-color.md).

 

La lunghezza massima è unbounded.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. suggerimento** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





