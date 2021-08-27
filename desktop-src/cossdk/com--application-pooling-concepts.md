---
description: Il pool di applicazioni COM+ consente la scalabilità dei processi a thread singolo, analogamente al modo in cui il pool di thread consente la scalabilità degli oggetti a thread singolo.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Concetti relativi al pool di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aab46350e3c6084c0d5e8ca61d2f3c90d27e06795f7d08568ee4a7c1e0fc26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096911"
---
# <a name="com-application-pooling-concepts"></a>Concetti relativi al pool di applicazioni COM+

Il pool di applicazioni COM+ consente la scalabilità dei processi a thread singolo, analogamente al modo in cui il pool di thread consente la scalabilità degli oggetti a thread singolo. Il pool di applicazioni consente anche di eseguire il ripristino in caso di errori in singoli processi fornendo altri processi in esecuzione in grado di gestire le attivazioni.

> [!Note]  
> Le applicazioni di libreria hanno le proprietà di riciclo e pooling del processo host.

 

Tutti i metodi [**dell'interfaccia ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) supportano il pool di applicazioni.

Il pool di applicazioni COM+ è configurabile per ogni applicazione usando la proprietà ConcurrentApps [**dell'oggetto COMAdminCatalogObject**](comadmincatalogobject.md) nella [**raccolta Applications.**](applications.md) ConcurrentApps è un valore intero che specifica il numero massimo di processi Dllhost simultanei che devono essere avviati per il servizio delle attivazioni per un'applicazione. Questa proprietà può essere impostata tramite lo strumento di amministrazione Servizi componenti o a livello di codice.

Se la proprietà ConcurrentApps è impostata su 1, ovvero il valore predefinito, il servizio Pool di applicazioni COM+ è disabilitato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività del pool di applicazioni COM+](com--application-pooling-tasks.md)
</dt> <dt>

[Concetti relativi al riciclo delle applicazioni COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



