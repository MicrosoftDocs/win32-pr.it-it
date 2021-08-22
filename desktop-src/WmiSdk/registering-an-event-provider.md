---
description: Per creare un provider di eventi WMI, è necessario registrare \_ \_ l'istanza win32Provider che rappresenta il provider usando \_ \_ un'istanza di EventProviderRegistration.
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
ms.openlocfilehash: 44c6521e56441c929ef108ce4c4b624c11b06ca26dc508c8f2f924e2f87babba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992511"
---
# <a name="registering-an-event-provider"></a>Registrazione di un provider di eventi

Per creare un [*provider di eventi*](gloss-e.md) WMI, è necessario registrare l'istanza [**\_ \_ win32Provider**](--win32provider.md) che rappresenta il provider usando un'istanza di [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md). Come oggetto COM, il provider deve registrarsi con il sistema operativo e WMI. La procedura seguente presuppone che il processo di registrazione sia già stato implementato come descritto in [Registrazione di un provider](registering-a-provider.md).

La procedura seguente descrive come registrare un provider di eventi.

**Per registrare un provider di eventi**

1.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) che descrive il provider.
2.  Creare un'istanza della [**\_ \_ classe EventProviderRegistration**](--eventproviderregistration.md) che descrive il set di funzionalità del provider.

    La [**\_ \_ classe EventProviderRegistration**](--eventproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration.**](--objectproviderregistration.md) Le proprietà locali della **\_ \_ classe EventProviderRegistration** sono il percorso dell'oggetto per il provider e un elenco di query che descrivono gli eventi supportati dal provider. Per altre informazioni, vedere [Esecuzione di query su WMI.](querying-wmi.md)

3.  Caricare l'implementazione [**\_ \_ delle classi Win32Provider**](--win32provider.md) [**\_ \_ ed EventProviderRegistration**](--eventproviderregistration.md) nel repository WMI.

    WMI usa la definizione della classe per registrare e accedere al provider di eventi. Per altre informazioni, vedere [Registrazione di un provider](registering-a-provider.md).

L'esempio di codice seguente descrive un'implementazione di [**\_ \_ una classe Win32Provider**](--win32provider.md) e di [**\_ \_ una classe EventProviderRegistration.**](--eventproviderregistration.md)

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

La prima query indica che il provider genera tutte le notifiche degli eventi per la classe di evento estensiva FaxEvent. Poiché usa l'operatore ISA, la seconda query implica che il provider genera notifiche per tutti gli eventi di creazione dell'istanza per la classe [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e tutte le relative sottoclassi.

Quando un provider si registra per fornire un evento intrinseco, l'evento deve essere applicato a tutte le istanze di una classe. In altre parole, non è possibile scrivere una query per fornire eventi di creazione dell'istanza solo per alcune unità disco appartenenti alla [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

 

 
