---
description: Una funzione del programma di installazione può visualizzare una finestra di dialogo di messaggio di errore che restituisce uno degli errori seguenti. Una casella di errore viene visualizzata solo se il livello dell'interfaccia utente è a livello completo, ridotto o di base. Per ulteriori informazioni, vedere livelli di interfaccia utente.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Messaggi di errore visualizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309498"
---
# <a name="displayed-error-messages"></a>Messaggi di errore visualizzati

Una [funzione del programma di installazione](installer-function-reference.md) può visualizzare una finestra di dialogo di messaggio di errore che restituisce uno degli errori seguenti. Una casella di errore viene visualizzata solo se il livello dell'interfaccia utente è a livello completo, ridotto o di base. Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Le funzioni del programma di installazione visualizzano solo i messaggi di errore riportati nella tabella seguente. Per gli errori non presenti nell'elenco, il chiamante della funzione è responsabile della gestione della visualizzazione dei messaggi di errore.



| Codice di errore               | Errore                        |
|--------------------------|------------------------------|
| ERRORE \_ installazione \_ sospensione  | L'installazione è stata sospesa.   |
| ERRORE di \_ installazione di \_ USEREXIT | L'utente ha terminato l'installazione. |
| ERRORE di \_ installazione \_  | Installazione non riuscita.              |



 

 

 



