---
description: Per creare un provider di metodi WMI è necessario registrare \_ \_ l'istanza Win32Provider che rappresenta il provider usando un'istanza di \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrazione di un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a85fb93a30f6a996dd8e7255cc53f7a58a7fe37df35eb16bdca8de038e8704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992561"
---
# <a name="registering-a-method-provider"></a>Registrazione di un provider di metodi

Per creare un [*provider di metodi*](gloss-m.md) WMI è necessario registrare l'istanza [**\_ \_ win32Provider**](--win32provider.md) che rappresenta il provider usando un'istanza di [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md). Dopo aver creato un'istanza [**\_ \_ di Win32Provider**](--win32provider.md), è necessario registrare tale provider con WMI. Come oggetto COM, il provider deve registrarsi con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [Registrazione di un provider](registering-a-provider.md).

Nella procedura seguente viene descritto come registrare un provider di metodi.

**Per registrare un provider di metodi**

1.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) che descrive il provider.

    La classe di sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration.**](--objectproviderregistration.md) Tuttavia, l'unica proprietà pertinente per un provider di metodi è il percorso dell'oggetto dell'istanza [**\_ \_ di Win32Provider.**](--win32provider.md)

2.  Creare un'istanza della [**\_ \_ classe MethodProviderRegistration**](--methodproviderregistration.md) che descrive il set di funzionalità del provider.

    Assicurarsi di contrassegnare la classe con entrambi i [**qualificatori Dynamic**](dynamic-qualifier.md) [**e Provider.**](/windows/desktop/api/Provider/nl-provider-provider) Il **qualificatore dinamico** segnala che WMI deve utilizzare un provider per recuperare le istanze della classe. Il **qualificatore** Provider specifica il nome del provider che WMI deve utilizzare.

Nell'esempio di codice seguente viene descritto come registrare un provider di metodi.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



