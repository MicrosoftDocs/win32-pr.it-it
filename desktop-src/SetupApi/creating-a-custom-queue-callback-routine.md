---
description: Oltre a usare il callback della coda predefinito, è possibile scrivere una routine di callback personalizzata.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Creazione di una routine di callback della coda personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0602e32ef97ea962ca91375318bb563c0809da0dc4877aa6c9439644b52408e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887508"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Creazione di una routine di callback della coda personalizzata

Oltre a usare il callback della coda predefinito, è possibile scrivere una routine di callback personalizzata. Questa funzione deve avere lo stesso formato di [*FileCallback.*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a) Ciò è utile se è necessaria una routine di callback per gestire una notifica in modo diverso da quello fornito dalla routine di callback della coda predefinita.

Se è necessario modificare solo una piccola parte del comportamento della routine di callback della coda predefinita, è possibile creare una routine di callback personalizzata per filtrare le notifiche, gestendo solo quelle che richiedono un comportamento speciale e chiamando [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) per le altre.

Ad esempio, se si desidera gestire gli errori di eliminazione dei file personalizzati, è possibile creare una funzione di callback personalizzata, *MyCallback*. Questa funzione intercetta ed elabora [**le notifiche SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) e chiama la funzione di callback della coda predefinita per tutte le altre notifiche. *MyCallback restituisce* un valore per le notifiche di errore di eliminazione. Per tutte le altre notifiche, *MyCallback passa* qualsiasi valore della routine di callback della coda predefinita restituita alla coda.

Questo flusso di controllo è illustrato nel diagramma seguente.

![Frecce e caselle che mostrano il flusso di dati per la funzione di callback personalizzata](images/callback.png)

> [!IMPORTANT]
> Se la funzione di callback personalizzata chiama la routine di callback della coda predefinita, deve passare il puntatore void restituito da [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) alla routine di callback predefinita.

 

 

 
