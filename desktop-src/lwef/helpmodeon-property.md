---
title: Proprietà HelpModeOn
description: Proprietà HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710924"
---
# <a name="helpmodeon-property"></a>Proprietà HelpModeOn

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se la modalità della Guida sensibile al contesto è impostata su on per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri ("*** CharacterID * * *"). HelpModeOn*( *  \[  =  *booleano* )\]



| Parte      | Descrizione                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se la modalità della Guida sensibile al contesto è on. Valore **true** La modalità della guida è on. <br/> **False** (impostazione predefinita) la modalità della guida è disattivata.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si imposta questa proprietà su **true**, il puntatore del mouse assume la forma dell'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu di scelta rapida per il carattere. Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu popup del carattere, il server attiva l'evento [**HelpComplete**](helpcomplete-event.md) e chiude la modalità della guida.

In modalità guida, il server non invia gli eventi [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)e [**Command**](command-event.md) , a meno che non si imposti la proprietà [**AutoPopupMenu**](autopopupmenu-property.md) su **true**. In tal caso, il server invierà l'evento **Click** (non esce dalla modalità guida), ma solo per il pulsante destro del mouse per consentire la visualizzazione del menu a comparsa.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**Evento HelpComplete**](helpcomplete-event.md)


 

 





