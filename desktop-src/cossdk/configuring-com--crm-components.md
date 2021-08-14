---
description: I componenti CRM possono essere installati in un'applicazione server COM+ o in un'applicazione libreria COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configurazione dei componenti COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79f8c9716a9a4db2888231c886d3d1a4d929dd1a8dfb9f9f359ab03ec7670b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307450"
---
# <a name="configuring-com-crm-components"></a>Configurazione dei componenti COM+ CRM

I componenti CRM possono essere installati in un'applicazione server COM+ o in un'applicazione libreria COM+. Tuttavia, devono essere sempre eseguiti in un'applicazione server COM+. Se vengono installati in un'applicazione libreria COM+, non sono disponibili per l'uso nei processi client.

Se i componenti CRM sono installati in un'applicazione di libreria, sono disponibili per più di un'applicazione server. Se installati in un'applicazione server specifica, sono disponibili solo per l'applicazione server specifica.

Per abilitare l'uso di crm in un'applicazione server, seguire questa procedura:

1.  In Servizi componenti, nella pagina delle proprietà dell'applicazione server, fare clic **sulla scheda** Avanzate .

2.  Selezionare **l'opzione Enable compensating Resource Managers (Abilita gestori risorse** di compensazione) per l'applicazione server. Se questa opzione non è selezionata, i tentativi di utilizzare un SISTEMA CRM all'interno di questa applicazione server avranno esito negativo.

    > [!Note]  
    > Se installato in un'applicazione di libreria,  non è necessario selezionare l'opzione Abilita gestori risorse di compensazione per tale applicazione di libreria, ma questa opzione deve essere selezionata per l'applicazione server in cui è previsto l'esecuzione del sistema CRM.

     

È consigliabile che i componenti CRM Worker e CRM Compensator per un CRM specifico siano installati nella stessa applicazione.

Le impostazioni consigliate per i componenti CRM sono le seguenti.



| Componente           | Impostazioni                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **Ruolo di lavoro CRM**      | transaction = requiredsync = yesJIT = yesthreading model = Both (o modello di threading = Apartment)     |
| **CRM Compensator** | transaction = disabledsync = disabledJIT = nothreading model = Both (o modello di threading = Apartment) |



 

> [!Note]  
> I componenti che usano CRM devono specificare in modo esplicito un modello di threading quando vengono registrati. Il valore predefinito, 'Main Thread Apartment', non è supportato. Gli unici due modelli di threading supportati sono Apartment e Both.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alla Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



