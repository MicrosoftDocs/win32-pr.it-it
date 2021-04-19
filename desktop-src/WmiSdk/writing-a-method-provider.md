---
description: Un provider di metodi consente l'accesso WMI ai metodi di una classe. Ad esempio, una classe che rappresenta un'applicazione può disporre di un metodo che termina l'applicazione.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Scrittura di un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310317"
---
# <a name="writing-a-method-provider"></a>Scrittura di un provider di metodi

Un provider di metodi consente l'accesso WMI ai metodi di una classe. Ad esempio, una classe che rappresenta un'applicazione può disporre di un metodo che termina l'applicazione.

La modifica dell'ordine dei parametri di input e output del metodo durante l'aggiornamento di un provider di metodi esistente può causare un errore per le applicazioni che chiamano il metodo. L'ordine dei parametri di input o output viene stabilito dal valore del qualificatore [**ID**](standard-wmi-qualifiers.md) per ogni parametro. Il primo parametro ha un valore **ID** pari a zero. Aggiungere nuovi parametri di input alla fine dei parametri esistenti anziché inserirli nella sequenza già stabilita.

Nella procedura seguente viene descritto come implementare un provider di metodi.

**Per implementare un provider di metodi**

1.  Progettare e registrare il provider di classi con WMI.

    I provider di classi si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) . Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di metodi](registering-a-method-provider.md).

2.  Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    > [!Note]  
    > I provider di metodi sono vivamente invitati a usare il modello di multithreading "both".

     

3.  Implementare il metodo [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) per il provider.

    L'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di metodi. Per ulteriori informazioni, vedere [implementazione dell'interfaccia primaria per un provider di metodi](implementing-the-primary-interface-for-a-method-provider.md).

4.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per ulteriori informazioni, vedere [chiamata di un metodo](calling-a-method.md) e [gestione dei livelli di sicurezza in un provider](impersonating-a-client.md).

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client. Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).

5.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia. Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).

 

 



