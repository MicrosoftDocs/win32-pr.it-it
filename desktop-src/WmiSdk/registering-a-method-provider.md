---
description: Per creare un provider di metodi WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrazione di un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232395"
---
# <a name="registering-a-method-provider"></a>Registrazione di un provider di metodi

Per creare un [*provider di metodi*](gloss-m.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md). Dopo aver creato un'istanza di [**\_ \_ Win32Provider**](--win32provider.md), è necessario registrare il provider con WMI. Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).

Nella procedura riportata di seguito viene descritto come registrare un provider di metodi.

**Per registrare un provider di metodi**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.

    La classe di sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . Tuttavia, l'unica proprietà pertinente per un provider di metodi è il percorso dell'oggetto per l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) .

2.  Creare un'istanza della classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) che descrive il set di funzionalità del provider.

    Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](dynamic-qualifier.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Il qualificatore **dinamico** segnala che WMI deve usare un provider per recuperare le istanze della classe. Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.

Nell'esempio di codice seguente viene illustrato come registrare un provider di metodi.

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

 

 



