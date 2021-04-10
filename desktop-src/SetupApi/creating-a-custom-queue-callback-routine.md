---
description: Oltre a usare il callback della coda predefinito, è possibile scrivere una routine di callback personalizzata.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Creazione di una routine di callback della coda personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883585"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Creazione di una routine di callback della coda personalizzata

Oltre a usare il callback della coda predefinito, è possibile scrivere una routine di callback personalizzata. Questa funzione deve avere lo stesso formato di [*filecallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Questa operazione è utile se è necessaria una routine di callback per gestire una notifica in un modo diverso da quello fornito dalla routine di callback della coda predefinita.

Se è necessario modificare solo una piccola parte del comportamento predefinito della routine di callback della coda, è possibile creare una routine di callback personalizzata per filtrare le notifiche, gestendo solo quelle che richiedono un comportamento speciale e chiamando [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) per le altre.

Se, ad esempio, si desidera gestire in modo personalizzato gli errori di eliminazione dei file, è possibile creare una funzione di callback personalizzata, ovvero *callback*. Questa funzione intercetta ed elabora le [**notifiche \_ DELETEERROR di SPFILENOTIFY**](spfilenotify-deleteerror.md) e chiama la funzione di callback della coda predefinita per tutte le altre notifiche. Il *callback* restituisce un valore per le notifiche di errore Delete. Per tutte le altre notifiche, il *callback* passa qualsiasi valore che la routine di callback della coda predefinita ha restituito alla coda.

Questo flusso di controllo è illustrato nel diagramma seguente.

![frecce e caselle che mostrano il flusso di dati per la funzione di callback personalizzata](images/callback.png)

> [!IMPORTANT]
> Se la funzione di callback personalizzata chiama la routine di callback della coda predefinita, deve passare il puntatore void restituito da [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) alla routine di callback predefinita.

 

 

 
