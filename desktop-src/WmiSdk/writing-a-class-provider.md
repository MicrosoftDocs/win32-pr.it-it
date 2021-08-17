---
description: Un provider di classi gestisce una classe o una serie di classi per WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Scrittura di un provider di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45815c795b6f43f3e7ec99b9ce9535c4d14b2bc8426ea5ca6b44f736415bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311940"
---
# <a name="writing-a-class-provider"></a>Scrittura di un provider di classi

Un provider di classi gestisce una classe o una serie di classi per WMI. Un provider di classi può essere push o pull. ciò significa che può archiviare i propri dati o consentire a WMI di archiviare i relativi dati nel Windows Management Service. Anche se un provider di classi è installato in un computer specifico, può modificare le definizioni di classe in un'intera azienda. Di conseguenza, la maggior parte degli sviluppatori spesso non crea provider di classi.

Prima di costruire un provider di classi, verificare che le classi supportate siano effettivamente generate dinamicamente. Nella maggior parte dei casi, l'elenco delle classi è a modifica lenta e limitato. In questo caso, non è necessario creare un provider di classi. È invece possibile inserire le definizioni delle classi nel repository WMI usando l'API WMI o un file MOF.

Nella procedura seguente viene descritto come implementare un provider di classi.

**Per implementare un provider di classi**

1.  Determinare se il provider è un provider push o pull.

    Un provider pull fornisce i dati in modo dinamico in risposta a una richiesta dell'applicazione, mentre i provider push archiviano i dati una sola volta nel repository WMI. Per altre informazioni, vedere [Determinazione dello stato push o pull.](determining-push-or-pull-status.md)

2.  Progettare e registrare il provider di classi con WMI.

    I provider di classi registrano con WMI creando [**\_ \_ un'istanza Win32Provider**](--win32provider.md) e [**\_ \_ un'istanza ClassProviderRegistration.**](--classproviderregistration.md) Per altre informazioni, vedere [Registrazione di un provider di classi.](registering-a-class-provider.md)

3.  Implementare [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    WMI usa [**IWbemProviderInit per**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) caricare e inizializzare un provider. Se si progetta un provider di push, **IWbemProviderInit è** l'unica interfaccia che verrà implementata. Per altre informazioni, vedere [Inizializzazione di un provider.](initializing-a-provider.md)

    > [!Note]  
    > I provider di classi sono fortemente invitati a usare il modello di multithreading "Both".

     

4.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per altre informazioni, vedere [Chiamata di un metodo e](calling-a-method.md) gestione dei livelli di sicurezza in un [provider.](impersonating-a-client.md)

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per tale client. Per altre informazioni, vedere [Rappresentazione di un client.](impersonating-a-client.md)

5.  Implementare [**l'interfaccia IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per il provider.

    [**L'interfaccia IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di classi pull. Per altre informazioni, vedere [Implementazione dell'interfaccia primaria per un provider di classi.](implementing-the-primary-interface-for-a-class-provider.md)

6.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente da copiare. Per altre informazioni, vedere [Aggiornamento di un provider.](updating-a-provider.md)

 

 



