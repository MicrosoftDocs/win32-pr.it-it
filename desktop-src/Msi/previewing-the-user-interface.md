---
description: Il programma di installazione archivia tutte le informazioni sull'interfaccia utente nelle tabelle del database di installazione.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Visualizzazione in anteprima dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231861"
---
# <a name="previewing-the-user-interface"></a>Visualizzazione in anteprima dell'interfaccia utente

Il programma di installazione archivia tutte le informazioni sull' [interfaccia utente](user-interface.md) nelle tabelle del database di installazione. Per semplificare la progettazione dell'interfaccia utente, il programma di installazione fornisce anche una modalità di anteprima per la visualizzazione di queste informazioni. Nella procedura seguente viene descritto come abilitare la modalità di anteprima dell'interfaccia utente e visualizzare l'aspetto corrente delle finestre di dialogo e dei tabelloni.

**Per visualizzare l'interfaccia utente in modalità di anteprima**

1.  Abilitare la modalità di anteprima chiamando la funzione [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .
2.  Visualizzare le finestre di dialogo specifiche chiamando la funzione [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .
3.  Visualizzare manifesti specifici chiamando la funzione [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .

 

 



