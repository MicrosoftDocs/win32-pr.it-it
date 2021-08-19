---
description: Se questo bit è impostato, la finestra di dialogo è modale, non è possibile posizionare altre finestre di dialogo della stessa applicazione su di essa e la finestra di dialogo mantiene il controllo mentre è in esecuzione.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit di stile finestra di dialogo modale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3663445a81acf07aebd9961f8ddb048dc8c8f466968573ac2c45544d6bd79baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945478"
---
# <a name="modal-dialog-style-bit"></a>Bit di stile finestra di dialogo modale

Se questo bit è impostato, la finestra di dialogo è modale, non è possibile posizionare altre finestre di dialogo della stessa applicazione su di essa e la finestra di dialogo mantiene il controllo mentre è in esecuzione. Se questo bit non è impostato, il dialogo è non modali e altri dialognti della stessa applicazione possono essere spostati sopra di esso. Dopo aver creato e visualizzato una finestra di dialogo non modabile, l'interfaccia utente restituisce il controllo al programma di installazione. Il programma di installazione chiama quindi periodicamente l'interfaccia utente per aggiornare il dialogo e per offrire la possibilità di elaborare i messaggi. Non appena questa operazione viene eseguita, il controllo viene restituito al programma di installazione.

> [!Note]  
> Non devono essere presenti finestre di dialogo non modali in una sequenza di procedura guidata, perché restituirebbe il controllo al programma di installazione, terminando la sequenza della procedura guidata in modo prematura.

 

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



