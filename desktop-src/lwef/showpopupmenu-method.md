---
title: Metodo ShowPopupMenu
description: Metodo ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297847"
---
# <a name="showpopupmenu-method"></a>Metodo ShowPopupMenu

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Consente di visualizzare il menu di scelta rapida del carattere nella posizione specificata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri ("*** CharacterID ***"). ShowPopupMenu*** x, y*



| Parte | Descrizione                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Obbligatorio. Valore intero che indica la coordinata orizzontale (*x*) dello schermo per visualizzare il menu. È necessario specificare queste coordinate in pixel. |
| *y*  | Obbligatorio. Valore intero che indica la coordinata verticale (*y*) dello schermo per visualizzare il menu. È necessario specificare queste coordinate in pixel.   |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Agent Visualizza automaticamente il menu di scelta rapida del carattere quando l'utente fa clic con il pulsante destro del mouse sul carattere. Se si imposta [**AutoPopupMenu**](autopopupmenu-property.md) su **false**, è possibile usare questo metodo per visualizzare il menu.

Il menu rimane visualizzato fino a quando l'utente non seleziona un comando o Visualizza un altro menu. È possibile visualizzare un solo menu popup alla volta; Pertanto, le chiamate a questo metodo cancelleranno (rimuovere) il menu precedente.

Questo metodo deve essere chiamato solo quando l'applicazione client è il client attivo del carattere; in caso contrario, avrà esito negativo. Per determinare l'esito positivo di questo metodo, è possibile chiamarlo come funzione e restituirà un valore booleano che indica se il metodo ha avuto esito positivo.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Vedere anche

[**Proprietà AutoPopupMenu**](autopopupmenu-property.md)


 

 




