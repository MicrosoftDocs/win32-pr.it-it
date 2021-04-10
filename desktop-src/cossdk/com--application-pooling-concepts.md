---
description: Il pool di applicazioni COM+ consente la scalabilità dei processi a thread singolo, analogamente al modo in cui il pool di thread consente la scalabilità degli oggetti a thread singolo.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Concetti relativi al pool di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877518"
---
# <a name="com-application-pooling-concepts"></a>Concetti relativi al pool di applicazioni COM+

Il pool di applicazioni COM+ consente la scalabilità dei processi a thread singolo, analogamente al modo in cui il pool di thread consente la scalabilità degli oggetti a thread singolo. Il pool di applicazioni consente inoltre di risolvere gli errori nei singoli processi, fornendo altri processi in esecuzione in grado di gestire le attivazioni.

> [!Note]  
> Le applicazioni di libreria hanno le proprietà di riciclo e pool del processo host.

 

Tutti i metodi dell'interfaccia [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) supportano il pool di applicazioni.

Il pool di applicazioni COM+ è configurabile per applicazione tramite la proprietà ConcurrentApps dell'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) nella raccolta di [**applicazioni**](applications.md) . ConcurrentApps è un valore intero che specifica il numero massimo di processi Dllhost simultanei che devono essere avviati per attivare il servizio per un'applicazione. Questa proprietà può essere impostata utilizzando lo strumento di amministrazione Servizi componenti o a livello di codice.

Se la proprietà ConcurrentApps è impostata su 1, ovvero sul valore predefinito, il servizio pool di applicazioni COM+ è disabilitato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività del pool di applicazioni COM+](com--application-pooling-tasks.md)
</dt> <dt>

[Concetti relativi al riciclo delle applicazioni COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



