---
description: I componenti di CRM possono essere installati in un'applicazione server COM+ o in un'applicazione libreria COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configurazione dei componenti di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305227"
---
# <a name="configuring-com-crm-components"></a>Configurazione dei componenti di COM+ CRM

I componenti di CRM possono essere installati in un'applicazione server COM+ o in un'applicazione libreria COM+. Tuttavia, devono essere sempre eseguiti in un'applicazione server COM+. Se sono installate in un'applicazione libreria COM+, non sono disponibili per l'utilizzo nei processi client.

Se i componenti CRM installati in un'applicazione di libreria sono disponibili per più di un'applicazione server. Se installate in un'applicazione server specifica, sono disponibili solo per tale applicazione server specifica.

Per abilitare l'uso di un CRM in un'applicazione server, seguire questa procedura:

1.  In Servizi componenti, nella pagina Proprietà applicazione server, fare clic sulla scheda **Avanzate** .

2.  Selezionare l'opzione **Enable Compensating Resource managers** per l'applicazione server. Se questa opzione non è selezionata, i tentativi di usare un CRM in questa applicazione server avranno esito negativo.

    > [!Note]  
    > Se installato in un'applicazione libreria, non è necessario selezionare l'opzione **Abilita gestione risorse di compensazione** per l'applicazione della libreria, ma questa opzione deve essere selezionata per l'applicazione server in cui è previsto l'esecuzione del CRM.

     

Si consiglia di installare i componenti del ruolo di lavoro CRM e del compensatore CRM per un CRM specifico nella stessa applicazione.

Di seguito sono riportate le impostazioni consigliate per i componenti di CRM.



| Componente           | Impostazioni                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **Ruolo di lavoro CRM**      | Transaction = requiredsync = yesJIT = yesthreading Model = both (o Threading Model = Apartment)     |
| **Compensatore CRM** | Transaction = disabledsync = disabledJIT = nothreading Model = both (o Threading Model = Apartment) |



 

> [!Note]  
> I componenti che utilizzano CRM devono specificare in modo esplicito un modello di threading quando vengono registrati. Il valore predefinito ' Apartment thread principale ' non è supportato. Gli unici due modelli di threading supportati sono Apartment e both.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



