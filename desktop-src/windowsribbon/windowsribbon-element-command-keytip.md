---
title: Command.Keytip - proprietà
description: Rappresenta la descrizione comando per un controllo .
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Proprietà Command.Keytip Windows Ribbon
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d70edeae49a2acbd561bd4d56e32028852993cc524a0df3882e7e0b8a8da18b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964245"
---
# <a name="commandkeytip-property"></a>Command.Keytip - proprietà

Rappresenta la descrizione comando per un controllo .

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

Può verificarsi al massimo una volta per ogni [**elemento**](windowsribbon-element-command.md) Command.

**Command.Keytip** può contenere un valore di tipo *xs:string* vincolato a qualsiasi sequenza di caratteri Unicode, inclusi gli spazi vuoti.

Un **oggetto Command.Keytip può** iniziare con un numero solo se associato a un controllo all'interno di una scheda o della barra di accesso [rapido.](windowsribbon-controls-quickaccesstoolbar.md) [](windowsribbon-controls-tab.md)

Per visualizzare i suggerimenti tasto di scelta validi per lo stato corrente della barra multifunzione, premere e tenere premuto ALT. La schermata seguente mostra i suggerimenti tasto di scelta iniziali o di primo livello visualizzati in Microsoft Paint per Windows 7. Dopo aver selezionato un suggerimento tasto di scelta di primo livello, vengono visualizzati solo i suggerimenti tasto di scelta di secondo livello.

![descrizioni comandi di primo livello in Microsoft Paint per Windows 7](images/properties/ui-pkey-label-keytips.png)

**Command.Keytip funge** da tasto di scelta rapida per un comando, a meno che tale comando non venga esposto tramite una voce di menu. In questo caso, il framework ignora il valore **Command.Keytip** e usa invece un carattere preceduto da una e commerciale come specificato da [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md). Se non viene specificata alcuna e commerciale da **Command.LabelTitle** o ui PKEY Label, non viene esposta alcuna descrizione comando o \_ tasto di scelta \_ rapida.

Se non viene fornito alcun valore per **Command.Keytip,** [**l'elemento**](windowsribbon-element-string.md) figlio String è obbligatorio.

> [!Note]  
> Se **Command.Keytip** contiene sia un valore che un elemento figlio [**String,**](windowsribbon-element-string.md) **String** ha la precedenza.

 

Per impostazione predefinita, il framework usa le lettere seguenti per generare automaticamente i suggerimenti tasto di scelta:

-   **F** viene assegnato al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).
-   **Y** viene assegnato a qualsiasi comando che non dispone di un suggerimento tasto di scelta specificato dall'applicazione.
-   **Z** viene assegnato a ogni [controllo Gruppo](windowsribbon-controls-group.md) e non può essere personalizzato. Un suggerimento tasto di scelta gruppo viene visualizzato solo quando [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) per il controllo specifica **un'opzione Di** dimensioni popup. Per altre informazioni, vedere [Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento](windowsribbon-templates.md).

> [!Note]  
> Nessuna di queste lettere è riservata dal framework. Ognuno può essere assegnato a uno o più comandi in base alle esigenze.

 

Il framework risolve i conflitti di suggerimento tasto di scelta nei modi seguenti:

-   Se uno [](windowsribbon-controls-tab.md) o più controlli Tab sono associati allo stesso suggerimento tasto di scelta, viene aggiunto un numero a ogni suggerimento tasto di scelta, a partire da 1 e aumentando in sequenza (2, 3,...) per ogni controllo nell'ordine di dichiarazione. Se ai controlli Tab viene assegnata la lettera F come suggerimento tasto di scelta, al [menu](windowsribbon-controls-applicationmenu.md) dell'applicazione viene assegnato F1 con i suggerimenti tasto di scelta rimanenti regolati come descritto.
-   Quando è associato a un singolo controllo all'interno [di](windowsribbon-controls-tab.md)una scheda , la descrizione comando F è valida sia per il controllo che per il [menu dell'applicazione](windowsribbon-controls-applicationmenu.md). La descrizione comando predefinita del menu dell'applicazione non viene modificata, ma viene data la precedenza al controllo nella scheda attiva.
-   Se uno o più controlli all'interno di [una](windowsribbon-controls-tab.md) scheda sono associati allo stesso suggerimento tasto di scelta, il framework crea automaticamente il refactoring dei suggerimenti tasto di scelta di tali controlli, come descritto in precedenza.

> [!Note]  
> Una leggera variazione del colore del testo viene usata per evidenziare i suggerimenti tasto di scelta con refactoring in un'implementazione standard della barra multifunzione. Per un'implementazione della barra multifunzione non standard in cui il colore della barra multifunzione è stato personalizzato, questo comportamento del framework viene sostituito e tutte le descrizioni comandi vengono visualizzate con lo stesso colore del testo. Per altre informazioni, vedere [Personalizzazione dei colori della barra multifunzione.](ribbon-color.md)

 

La lunghezza massima è illimitata.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per un [**elemento Command**](windowsribbon-element-command.md) con una **dichiarazione Command.Keytip.**


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Suggerimento \_ per la chiave PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





