---
description: Un provider di classi gestisce una classe o una serie di classi per WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Scrittura di un provider di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313154"
---
# <a name="writing-a-class-provider"></a>Scrittura di un provider di classi

Un provider di classi gestisce una classe o una serie di classi per WMI. Un provider di classi può essere push o pull; ovvero può archiviare i propri dati o consentire a WMI di archiviare i dati nel servizio di gestione Windows. Anche se un provider di classi è installato in un computer specifico, può modificare le definizioni delle classi in un'intera azienda. Pertanto, la maggior parte degli sviluppatori spesso non crea provider di classi.

Prima di creare un provider di classi, verificare che le classi supportate siano effettivamente generate dinamicamente. Nella maggior parte dei casi, l'elenco delle classi è a modifica lenta e finito. In tal caso, non è necessario creare un provider di classi. In alternativa, è possibile inserire le definizioni delle classi nel repository WMI utilizzando l'API WMI o un file MOF.

Nella procedura seguente viene descritto come implementare un provider di classi.

**Per implementare un provider di classi**

1.  Determinare se il provider è un provider push o pull.

    Un provider di pull fornisce i dati in modo dinamico in risposta a una richiesta dell'applicazione, mentre i provider di push memorizzano i dati una volta nel repository WMI. Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).

2.  Progettare e registrare il provider di classi con WMI.

    I provider di classi si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e un'istanza di [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) . Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di classi](registering-a-class-provider.md).

3.  Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider. Se si progetta un provider di push, **IWbemProviderInit** è l'unica interfaccia che verrà implementata. Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).

    > [!Note]  
    > I provider di classi sono vivamente invitati a usare il modello di multithreading "both".

     

4.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per ulteriori informazioni, vedere [chiamata di un metodo](calling-a-method.md) e [gestione dei livelli di sicurezza in un provider](impersonating-a-client.md).

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client. Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).

5.  Implementare l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per il provider.

    L'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di classi pull. Per ulteriori informazioni, vedere [Implementing the primary interface for a class provider](implementing-the-primary-interface-for-a-class-provider.md).

6.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia. Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).

 

 



