---
description: La routine di callback della coda predefinita gestisce le notifiche inviate da SetupCommitFileQueue in modo generico.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Informazioni sulla routine di callback della coda predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879022"
---
# <a name="about-the-default-queue-callback-routine"></a>Informazioni sulla routine di callback della coda predefinita

La routine di callback della coda predefinita gestisce le notifiche inviate da [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in modo generico. Utilizzando la routine predefinita, si ottiene un'interfaccia utente pronta per la creazione di finestre di dialogo di configurazione comuni. Si consiglia di utilizzare la routine di callback della coda predefinita, sia per semplicità d'uso, sia per garantire un aspetto e un comportamento coerenti delle finestre di dialogo generate durante l'installazione.

La routine di callback predefinita richiede una struttura di contesto per la conservazione dei record interni. Inoltre, la coda passa informazioni aggiuntive relative alla notifica corrente in un set di parametri, *param1* e *param2*.

Se, ad esempio, la coda Invia una \_ notifica SPFILENOTIFY NEEDMEDIA alla routine di callback predefinita, *param1* punta a una struttura del [**\_ supporto di origine**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) che contiene informazioni sui supporti necessari e *param2* punta a una matrice di caratteri che può ricevere le nuove informazioni sul percorso dall'utente.

La routine di callback predefinita utilizza queste informazioni per richiedere all'utente di inserire il supporto di origine necessario, specificare un nuovo percorso, ignorare la copia del file corrente oppure annullare l'operazione corrente. La routine di callback della coda predefinita restituisce FILEOP \_ NEWPATH, FILEOP \_ doit, FILEOP \_ Skip o FILEOP \_ Abort alla coda, a seconda dell'azione assunta dall'utente.

Per informazioni sul modo in cui la routine di callback della coda predefinita gestisce ogni notifica della coda, vedere [notifiche della coda di file](file-queue-notifications.md).

Per informazioni sulle routine di callback della coda personalizzate, vedere [creazione di una routine di callback della coda personalizzata](creating-a-custom-queue-callback-routine.md).

 

 



