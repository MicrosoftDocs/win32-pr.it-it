---
description: Per creare un provider di consumer di eventi WMI, è necessario registrare l'istanza win32Provider che rappresenta il provider usando un'istanza di \_ \_ \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrazione di un provider di consumer di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1922970838b99e2a4a371ed7b00ae0f506a0381f0018509bfd6874074e0dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992542"
---
# <a name="registering-an-event-consumer-provider"></a>Registrazione di un provider di consumer di eventi

Per creare un [*provider di consumer*](gloss-e.md) di eventi WMI, è necessario registrare l'istanza [**\_ \_ win32Provider**](--win32provider.md) che rappresenta il provider usando un'istanza di [**\_ \_ EventConsumerProviderRegistration.**](--eventconsumerproviderregistration.md) Come oggetto COM, il provider deve registrarsi con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [Registrazione di un provider](registering-a-provider.md).

Nella procedura seguente viene descritto come registrare un provider di consumer di eventi.

**Per registrare un provider di consumer di eventi**

1.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) che descrive il provider.
2.  Creare un'istanza della [**\_ \_ classe EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) che descrive il set di funzionalità del provider.

    Le proprietà definite da [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) includono il percorso dell'oggetto al provider e i nomi delle classi consumer logiche supportate dal provider di consumer di eventi.

    Assicurarsi di contrassegnare la classe con entrambi i **qualificatori Dynamic** [**e Provider.**](/windows/desktop/api/Provider/nl-provider-provider) Il **qualificatore dinamico** segnala che WMI deve utilizzare un provider per recuperare le istanze della classe. Il **qualificatore** Provider specifica il nome del provider che WMI deve utilizzare.

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

 

 



