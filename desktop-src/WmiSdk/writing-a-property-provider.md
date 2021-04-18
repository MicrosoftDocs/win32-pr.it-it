---
description: Un provider di proprietà recupera e modifica i singoli valori delle proprietà per le istanze di una determinata classe archiviata nel repository WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Scrittura di un provider di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313153"
---
# <a name="writing-a-property-provider"></a>Scrittura di un provider di proprietà

Un provider di proprietà recupera e modifica i singoli valori delle proprietà per le istanze di una determinata classe archiviata nel repository WMI.

Nella procedura riportata di seguito viene descritto come creare un provider di proprietà.

**Per creare un provider di proprietà**

1.  Progettare e registrare il provider con WMI.

    I provider di istanze si registrano con WMI creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e una classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) . Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di proprietà](registering-a-property-provider.md).

2.  Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider. Si tratta di un'attività comune a tutti i provider. Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).

    > [!Note]  
    > Per i provider di proprietà si consiglia vivamente di utilizzare il modello di multithreading "both".

     

3.  Implementare l'interfaccia [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) per il provider.

    L'interfaccia [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) è l'interfaccia principale per un provider di proprietà. I due metodi principali sono [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty). Per ulteriori informazioni, vedere [implementazione dell'interfaccia principale per un provider di proprietà](implementing-the-primary-interface-for-a-property-provider.md).

4.  Aggiungere il codice aggiuntivo necessario per il provider.

    Quando si progetta il provider, è molto probabile che sia necessario chiamare le interfacce WMI. Per ulteriori informazioni, vedere [chiamata di un metodo](calling-a-method.md) e [gestione dei livelli di sicurezza in un provider](impersonating-a-client.md).

    Quando si recuperano informazioni per un client, potrebbe essere necessario accedere ai livelli di sicurezza per il client. Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).

5.  Sostituire il provider preesistente con il nuovo codice.

    Non è necessario eseguire questo passaggio se non si dispone di un provider preesistente per la copia. Per ulteriori informazioni, vedere [aggiornamento di un provider](updating-a-provider.md).

 

 



