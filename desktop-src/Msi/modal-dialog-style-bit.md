---
description: Se questo bit è impostato, la finestra di dialogo è modale, altre finestre di dialogo della stessa applicazione non possono essere posizionate sopra di esso e la finestra di dialogo mantiene il controllo mentre è in esecuzione.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit stile finestra di dialogo modale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529749"
---
# <a name="modal-dialog-style-bit"></a>Bit stile finestra di dialogo modale

Se questo bit è impostato, la finestra di dialogo è modale, altre finestre di dialogo della stessa applicazione non possono essere posizionate sopra di esso e la finestra di dialogo mantiene il controllo mentre è in esecuzione. Se questo bit non è impostato, la finestra di dialogo non è modale, altre finestre di dialogo della stessa applicazione possono essere spostate sopra di esso. Dopo la creazione e la visualizzazione di una finestra di dialogo non modale, l'interfaccia utente restituisce il controllo al programma di installazione. Il programma di installazione chiama quindi l'interfaccia utente periodicamente per aggiornare la finestra di dialogo e fornire la possibilità di elaborare i messaggi. Non appena viene eseguita questa operazione, il controllo viene restituito al programma di installazione.

> [!Note]  
> Non devono essere presenti finestre di dialogo non modali in una sequenza della procedura guidata, poiché questo restituisce il controllo al programma di installazione, terminando la sequenza della procedura guidata in modo anomalo.

 

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



