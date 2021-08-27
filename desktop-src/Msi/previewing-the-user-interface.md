---
description: Il programma di installazione archivia tutte le informazioni sull'interfaccia utente nelle tabelle del database di installazione.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Anteprima del Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738387ac834d4e9c26f4a413755dce0c5abdc5e421cc4ef88b1f9b41054f201d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082661"
---
# <a name="previewing-the-user-interface"></a>Anteprima del Interfaccia utente

Il programma di installazione archivia tutte le informazioni [sull'interfaccia](user-interface.md) utente nelle tabelle del database di installazione. Per facilitare la progettazione dell'interfaccia utente, il programma di installazione offre anche una modalità di anteprima per la visualizzazione di queste informazioni. La procedura seguente descrive come abilitare la modalità di anteprima dell'interfaccia utente e visualizzare l'aspetto corrente delle finestre di dialogo e dei manifesti.

**Per visualizzare l'interfaccia utente in modalità di anteprima**

1.  Abilitare la modalità di anteprima chiamando la [**funzione MsiEnableUIPreview.**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
2.  Visualizzare le finestre di dialogo specifiche chiamando la [**funzione MsiPreviewDialog.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
3.  Visualizzare manifesti pubblicitari specifici chiamando la [**funzione MsiPreviewBillboard.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)

 

 



