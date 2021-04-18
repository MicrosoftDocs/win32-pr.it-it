---
description: Un provider di istanze fornisce istanze di una o più classi specificate.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Scrittura di un provider di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313677"
---
# <a name="writing-an-instance-provider"></a>Scrittura di un provider di istanze

Un provider di istanze fornisce istanze di una o più classi specificate. Un provider di istanze, ad esempio, può fornire informazioni riguardanti una CPU o un altro tipo di hardware. Poiché gli oggetti gestiti da un provider di istanze tendono a essere modificati a intervalli regolari, tutti i provider di istanze sono considerati provider di pull. ovvero un provider che recupera dinamicamente le informazioni relative a un oggetto gestito ogni volta che WMI esegue una richiesta di informazioni. Il nome deriva dal concetto che WMI estrae le informazioni dal provider per conto di una richiesta client. Grazie alla tecnologia pull, un provider di istanze può supportare il recupero, l'enumerazione, la modifica, l'eliminazione e l'elaborazione di query di un'istanza specifica.

I provider a prestazioni elevate possono aumentare l'efficienza di un provider di istanze o accedere a livello di codice ai dati visualizzati in Monitor di sistema. Per ulteriori informazioni, vedere [creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).

Nella procedura riportata di seguito viene descritto come scrivere un provider di istanze.

**Per scrivere un provider di istanze**

1.  [Registrare il provider con WMI](registering-an-instance-provider.md).

    I provider di istanze si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

2.  [Inizializzare il provider](initializing-a-provider.md).

    WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider. Si tratta di un'attività comune a tutti i provider.

    > [!Note]  
    > I provider di istanze sono vivamente invitati a usare il modello di multithreading "both".

     

3.  [Implementare l'interfaccia IWbemServices per il provider](implementing-the-primary-interface-for-an-instance-provider.md).

    L'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di istanze.

4.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per ulteriori informazioni, vedere [effettuare chiamate a WMI](making-calls-to-wmi.md).

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client. Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).

5.  Se necessario, [implementare l'interfaccia a prestazioni elevate](improving-the-efficiency-of-an-instance-provider.md).

    L'interfaccia a prestazioni elevate aumenta la velocità con cui il provider può rispondere alle richieste provenienti da WMI.

6.  Se necessario, [implementare il supporto per gli aggiornamenti parziali dell'istanza](supporting-partial-instance-operations.md).

    Come suggerisce il nome, un aggiornamento parziale dell'istanza è una tecnica utilizzata per aggiornare solo parte di un'istanza. Per ulteriori informazioni sulla chiamata di un'istanza parziale da un client, vedere [aggiornamento di una parte di un'istanza](updating-part-of-an-instance.md) e [recupero di parte di un'istanza di WMI](retrieving-part-of-an-instance.md).

7.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia. Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).

 

 



