---
description: Se questo bit è impostato, la finestra di dialogo è una finestra di dialogo di errore.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit di stile della finestra di dialogo di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f9c244e0f7905b72faf53306a7556ac8f9bb718c48666630751a5c0b20762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913491"
---
# <a name="error-dialog-style-bit"></a>Bit di stile della finestra di dialogo di errore

Se questo bit è impostato, la finestra di dialogo è una finestra di dialogo di errore.

Con questo stile può essere presente più di una finestra di dialogo. La **proprietà ErrorDialog** determina quale finestra di dialogo viene usata come finestra di dialogo di errore. La finestra di dialogo selezionata può essere solo una di quelle per cui è impostato questo bit di stile. La finestra di dialogo di errore deve avere un controllo di testo statico denominato ErrorText. Questo controllo riceve il testo del messaggio di errore. La finestra di dialogo deve avere anche i sette pulsanti di comando corrispondenti ai possibili valori restituiti. Il messaggio di errore determina quali di questi pulsanti vengono effettivamente visualizzati. I pulsanti visualizzati vengono ridisporti in modo che siano distribuiti uniformemente nella finestra di dialogo. Questa riorganizzazione modifica la coordinata X dei pulsanti, ma non le altre tre coordinate. È pertanto consigliabile non creare altri controlli nella stessa area orizzontale della finestra di dialogo dei pulsanti. Se il messaggio di errore non specifica alcun pulsante, **viene** visualizzato il pulsante OK. I **valori del** pulsante Predefinito, Primo controllo attivo e Annulla vengono ignorati per una finestra di dialogo di errore.  Il **pulsante** Predefinito definito nel messaggio di errore verrà assegnato a tutti e tre i valori. L'effetto del push di questi pulsanti deve essere definito nella tabella [ControlEvent](controlevent-table.md) esattamente come per tutti gli altri pulsanti. Il titolo del dialogo viene creato in modo simile ad altri dialoghe. Può essere sovrascritto dal messaggio di errore se specifica un testo di intestazione dopo l'elenco di pulsanti.

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **MsidbDialogAttributesError** |



 

 

 



