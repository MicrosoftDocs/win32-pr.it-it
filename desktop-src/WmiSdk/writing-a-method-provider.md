---
description: Un provider di metodi consente l'accesso WMI ai metodi di una classe. Ad esempio, una classe che rappresenta un'applicazione può avere un metodo che termina l'applicazione.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Scrittura di un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea5121d4a9438744ad62b666e62d4ffa90c39428020d3e39c80a6de26e295959
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311930"
---
# <a name="writing-a-method-provider"></a>Scrittura di un provider di metodi

Un provider di metodi consente l'accesso WMI ai metodi di una classe. Ad esempio, una classe che rappresenta un'applicazione può avere un metodo che termina l'applicazione.

La modifica dell'ordine dei parametri di input e di output del metodo durante l'aggiornamento di un provider di metodi esistente può causare errori per le applicazioni che chiamano il metodo . L'ordine dei parametri di input o di output viene stabilito dal valore del qualificatore [**ID**](standard-wmi-qualifiers.md) in ogni parametro. Il primo parametro ha un **valore ID** pari a zero. Aggiungere nuovi parametri di input alla fine dei parametri esistenti anziché inserirli nella sequenza già stabilita.

La procedura seguente descrive come implementare un provider di metodi.

**Per implementare un provider di metodi**

1.  Progettare e registrare il provider di classi con WMI.

    I provider di classi si registrano con WMI creando [**\_ \_ un'istanza Win32Provider**](--win32provider.md) e una [**\_ \_ classe MethodProviderRegistration.**](--methodproviderregistration.md) Per altre informazioni, vedere [Registrazione di un provider di metodi](registering-a-method-provider.md).

2.  Implementare [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    > [!Note]  
    > I provider di metodi sono fortemente invitati a usare il modello di multithreading "Both".

     

3.  Implementare [**il metodo IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) per il provider.

    [**L'interfaccia IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è l'interfaccia principale per un provider di metodi. Per altre informazioni, vedere [Implementazione dell'interfaccia primaria per un provider di metodi](implementing-the-primary-interface-for-a-method-provider.md).

4.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per altre informazioni, vedere [Chiamata di un metodo e](calling-a-method.md) gestione dei livelli di sicurezza in un [provider](impersonating-a-client.md).

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per tale client. Per altre informazioni, vedere [Rappresentazione di un client](impersonating-a-client.md).

5.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente su cui eseguire la copia. Per altre informazioni, vedere [Aggiornamento di un provider](updating-a-provider.md).

 

 



