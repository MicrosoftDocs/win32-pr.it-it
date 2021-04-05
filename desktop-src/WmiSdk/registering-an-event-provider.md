---
description: Per creare un provider di eventi WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ EventProviderRegistration.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrazione di un provider di eventi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131918"
---
# <a name="registering-an-event-provider"></a>Registrazione di un provider di eventi

Per creare un [*provider di eventi*](gloss-e.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md). Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).

Nella procedura riportata di seguito viene descritto come registrare un provider di eventi.

**Per registrare un provider di eventi**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.
2.  Creare un'istanza della classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) che descrive il set di funzionalità del provider.

    La classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . Le proprietà locali della classe **\_ \_ EventProviderRegistration** sono il percorso dell'oggetto per il provider e un elenco di query che descrivono gli eventi supportati dal provider. Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).

3.  Caricare l'implementazione delle classi [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) nel repository WMI.

    WMI utilizza la definizione della classe per registrare e accedere al provider di eventi. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).

Nell'esempio di codice seguente viene descritta un'implementazione di una classe [**\_ \_ Win32Provider**](--win32provider.md) e di una classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

La prima query indica che il provider genera tutte le notifiche degli eventi per la classe di evento estrinseca FaxEvent. Poiché usa l'operatore ISA, la seconda query implica che il provider genera notifiche per tutti gli eventi di creazione dell'istanza per la classe [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e per tutte le relative sottoclassi.

Quando un provider viene registrato per fornire un evento intrinseco, l'evento deve essere applicato a tutte le istanze di una classe. In altre parole, non è possibile scrivere una query per fornire eventi di creazione di istanze solo per alcune unità disco che appartengono alla classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

 

 
