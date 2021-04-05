---
title: Enumerazione delle attività
description: Utilità di pianificazione 1,0 fornisce un oggetto di enumerazione per l'enumerazione delle attività nella cartella delle attività pianificate.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- Enumerazione delle attività Utilità di pianificazione
- Enumerazione delle attività Utilità di pianificazione, descritta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045009"
---
# <a name="enumerating-tasks"></a>Enumerazione delle attività

Utilità di pianificazione 1,0 fornisce un oggetto di enumerazione per l'enumerazione delle attività nella [*cartella delle attività pianificate*](s.md).

> [!Note]  
> Per un computer Windows Server 2003, Windows XP o Windows 2000 per creare, monitorare o controllare le attività in un computer con Windows Vista, è necessario completare alcune operazioni sul computer Windows Vista. Per altre informazioni, vedere [Tasks](tasks.md) (Attività).

 

## <a name="using-the-enumeration-object"></a>Utilizzo dell'oggetto Enumeration

L'interfaccia [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) di questo oggetto fornisce i metodi per enumerare le attività nella cartella, reimpostando la sequenza di enumerazione sull'inizio dell'elenco, ignorando le attività e creando una copia dell'oggetto di enumerazione corrente per un uso successivo.

Per informazioni sull'enumerazione delle attività nella cartella delle attività pianificate, vedere [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).

Per informazioni sulla reimpostazione dell'enumerazione all'inizio dell'elenco, vedere [**IEnumWorkItems:: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).

Per informazioni sulle attività ignorate, vedere [**IEnumWorkItems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).

Per informazioni su come creare una copia dell'oggetto di enumerazione corrente, vedere [**IEnumWorkItems:: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).

Per un esempio di enumerazione delle attività nella cartella delle attività pianificate, vedere [esempio di enumerazione](enumerating-tasks-example.md)delle attività.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sull'attività Utilità di pianificazione 1,0](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




