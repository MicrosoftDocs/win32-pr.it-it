---
description: Per creare un provider di consumer di eventi WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrazione di un provider di consumer di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755047"
---
# <a name="registering-an-event-consumer-provider"></a>Registrazione di un provider di consumer di eventi

Per creare un [*provider di consumer di eventi*](gloss-e.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md). Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).

Nella procedura seguente viene descritto come registrare un provider di consumer di eventi.

**Per registrare un provider di consumer di eventi**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.
2.  Creare un'istanza della classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) che descrive il set di funzionalità del provider.

    Le proprietà definite da [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) includono il percorso dell'oggetto per il provider e i nomi delle classi di consumer logiche supportate dal provider di consumer di eventi.

    Assicurarsi di contrassegnare la classe con i qualificatori **dinamici** e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Il qualificatore **dinamico** segnala che WMI deve usare un provider per recuperare le istanze della classe. Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.

Nell'esempio di codice seguente viene illustrato come registrare un provider di consumer di eventi.

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



