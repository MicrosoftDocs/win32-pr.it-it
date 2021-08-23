---
title: Metodo ShowPopupMenu
description: Metodo ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cfd080adcf0158a628f019b4d48be5cd10b9c5b47d7a4b71ccd2393ad83ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600991"
---
# <a name="showpopupmenu-method"></a>Metodo ShowPopupMenu

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Visualizza il menu a comparsa del carattere nella posizione specificata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). ShowPopupMenu_ * _x, y_



| Parte | Descrizione                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Obbligatorio. Valore intero che indica la coordinata orizzontale (*x*) dello schermo per visualizzare il menu. Queste coordinate devono essere specificate in pixel. |
| *y*  | Obbligatorio. Valore intero che indica la coordinata verticale (*y*) dello schermo per visualizzare il menu. Queste coordinate devono essere specificate in pixel.   |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Agent visualizza automaticamente il menu a comparsa del carattere quando l'utente fa clic con il pulsante destro del mouse sul carattere. Se si imposta [**AutoPopupMenu**](autopopupmenu-property.md) su **False,** è possibile usare questo metodo per visualizzare il menu.

Il menu rimane visualizzato fino a quando l'utente non seleziona un comando o non visualizza un altro menu. È possibile visualizzare un solo menu a comparsa alla volta. Pertanto, le chiamate a questo metodo annullano (rimuovono) il menu precedente.

Questo metodo deve essere chiamato solo quando l'applicazione client è il client attivo del carattere. in caso contrario, ha esito negativo. Per determinare l'esito positivo di questo metodo, è possibile chiamarlo come funzione e restituirà un valore booleano che indica se il metodo ha avuto esito positivo.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Vedere anche

[**Proprietà AutoPopupMenu**](autopopupmenu-property.md)


 

 




