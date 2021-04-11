---
description: Quando il Windows Installer elabora lo script di installazione per l'installazione di un prodotto o di un'applicazione, genera contemporaneamente uno script di rollback e salva una copia di ogni file eliminato durante l'installazione.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Rollback dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130666"
---
# <a name="rollback-installation"></a>Rollback dell'installazione

Quando il Windows Installer elabora lo script di installazione per l'installazione di un prodotto o di un'applicazione, genera contemporaneamente uno script di rollback e salva una copia di ogni file eliminato durante l'installazione. Questi file vengono conservati in una directory di sistema nascosta e vengono eliminati automaticamente al termine dell'installazione. Se tuttavia l'installazione ha esito negativo, il programma di installazione esegue automaticamente un'installazione di rollback che restituisce lo stato originale del sistema.

Il rollback automatico di un'installazione non riuscita è il comportamento predefinito del programma di installazione. Per disabilitare il rollback durante un'installazione, usare uno dei seguenti elementi:

-   [**Proprietà DISABLEROLLBACK**](-disablerollback.md)
-   [**Proprietà PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [Azione DisableRollback](disablerollback-action.md)
-   [DisableRollback](disablerollback.md)
-   [ControlEvent EnableRollback](enablerollback-controlevent.md)

Ogni volta che il rollback è disabilitato, il programma di installazione imposta la proprietà [**RollbackDisabled**](rollbackdisabled.md) .

Se un'installazione utilizza [azioni personalizzate](custom-actions.md), per utilizzare la funzionalità di rollback è necessaria la creazione aggiuntiva del pacchetto di installazione. Per altre informazioni, vedere [rollback delle azioni personalizzate](rollback-custom-actions.md).

 

 



