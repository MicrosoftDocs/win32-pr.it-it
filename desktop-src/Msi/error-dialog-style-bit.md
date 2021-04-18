---
description: Se questo bit è impostato, la finestra di dialogo è una finestra di dialogo di errore.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit di stile della finestra di dialogo di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308330"
---
# <a name="error-dialog-style-bit"></a>Bit di stile della finestra di dialogo di errore

Se questo bit è impostato, la finestra di dialogo è una finestra di dialogo di errore.

Con questo stile può essere presente più di una finestra di dialogo. La proprietà **ErrorDialog** determina quale finestra di dialogo viene utilizzata come finestra di dialogo di errore. La finestra di dialogo selezionata può essere solo una di quelle per cui è impostato questo bit di stile. La finestra di dialogo di errore deve avere un controllo testo statico denominato ErrorText. Questo controllo riceve il testo del messaggio di errore. Nella finestra di dialogo devono essere presenti anche i sette pulsanti di push corrispondenti ai valori restituiti possibili. Il messaggio di errore determina quale di questi pulsanti è effettivamente visualizzato. I pulsanti visualizzati vengono ridisposti in modo che siano distribuiti uniformemente nella finestra di dialogo. Questa ridisposizione modifica la coordinata X dei pulsanti, ma non le altre tre coordinate. È pertanto consigliabile che non venga creato alcun altro controllo nella stessa area orizzontale della finestra di dialogo dei pulsanti. Se il messaggio di errore non specifica alcun pulsante, viene visualizzato il pulsante **OK** . Il pulsante **predefinito** , i valori primo controllo attivo e pulsante **Annulla** vengono ignorati per una finestra di dialogo di errore. Il pulsante **predefinito** definito nel messaggio di errore verrà assegnato a tutti e tre i valori. L'effetto del push di questi pulsanti deve essere definito nella [tabella ControlEvent](controlevent-table.md) esattamente come per tutti gli altri pulsanti. Il titolo della finestra di dialogo viene creato in modo analogo ad altre finestre di dialogo. Può essere sovrascritto dal messaggio di errore se specifica un testo dell'intestazione dopo l'elenco dei pulsanti.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **msidbDialogAttributesError** |



 

 

 



