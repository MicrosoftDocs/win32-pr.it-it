---
title: Proprietà HelpModeOn
description: Proprietà HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489de1893e96bf2d4cc38ef9e788a726db8b9fd4dfbdc9ae3cd1b60f9bc02f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962741"
---
# <a name="helpmodeon-property"></a>Proprietà HelpModeOn

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se la modalità Guida sensibile al contesto è attivata per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). HelpModeOn_ *  \[  =  *booleano*\]



| Parte      | Descrizione                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se la modalità Guida sensibile al contesto è attivata. **True** La modalità Guida è attivata. <br/> **False** (impostazione predefinita) La modalità Guida è disattivata.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si imposta questa proprietà su **True,** il puntatore del mouse passa all'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu a comparsa per il carattere. Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu a comparsa del carattere, il server attiva l'evento [**HelpComplete**](helpcomplete-event.md) e esce dalla modalità Guida.

In modalità Guida il server non invia gli eventi [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)e [**Command,**](command-event.md) a meno che non si imposta la [**proprietà AutoPopupMenu**](autopopupmenu-property.md) su **True**. In tal caso, il server invierà l'evento **Click** (non esce dalla modalità Guida), ma solo per il pulsante destro del mouse per consentire la visualizzazione del menu a comparsa.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**Evento HelpComplete**](helpcomplete-event.md)


 

 





