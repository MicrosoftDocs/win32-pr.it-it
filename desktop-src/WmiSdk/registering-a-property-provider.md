---
description: Per creare un provider di proprietà WMI è necessario registrare l'istanza win32Provider che rappresenta \_ \_ il provider usando un'istanza \_ \_ di PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrazione di un provider di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbbec33f81fdfa9c1d32b20f2f5cff44566c417b1311c3429bbfaa400b68625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554209"
---
# <a name="registering-a-property-provider"></a>Registrazione di un provider di proprietà

Per creare un [*provider di proprietà*](gloss-p.md) WMI è necessario registrare l'istanza [**\_ \_ win32Provider**](--win32provider.md) che rappresenta il provider usando un'istanza di [**\_ \_ PropertyProviderRegistration.**](--propertyproviderregistration.md) Come oggetto COM, il provider deve registrarsi con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [Registrazione di un provider](registering-a-provider.md).

Nella procedura seguente viene descritto come registrare un provider di proprietà.

**Per registrare un provider di proprietà**

1.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) che descrive il provider di proprietà.

    La [**\_ \_ classe Win32Provider**](--win32provider.md) accetta i valori predefiniti per altre proprietà, ad esempio **il valore TRUE** per la proprietà **Pure.** Per altre informazioni, vedere [**\_ \_ Win32Provider.**](--win32provider.md)

2.  Creare un'istanza della [**\_ \_ classe PropertyProviderRegistration**](--propertyproviderregistration.md) che descrive il set di funzionalità del provider.

    La [**\_ \_ classe PropertyProviderRegistration**](--propertyproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration,**](--objectproviderregistration.md) che fornisce valori booleani che indicano il supporto per particolari funzionalità e una matrice di stringhe per indicare il supporto delle query.

    Assicurarsi di contrassegnare la classe con entrambi i [**qualificatori Dynamic**](dynamic-qualifier.md) [**e Provider.**](/windows/desktop/api/Provider/nl-provider-provider) Il **qualificatore** dinamico segnala che WMI deve utilizzare un provider dinamico per recuperare le istanze della classe che contengono le proprietà supportate. Il **qualificatore** Provider specifica il nome del provider che WMI deve utilizzare.

WMI chiama NewQuery su un provider di eventi quando un consumer client registra una query di filtro eventi che contiene riferimenti a eventi supportati da tale provider di eventi. Il provider di eventi responsabile degli eventi di modifica dell'istanza per la classe EmailClass può quindi essere configurato in modo da generare notifiche solo per il mittente. Quando il provider riceve una query che richiede la notifica delle modifiche alla proprietà dell'oggetto, il provider può iniziare a generare tali notifiche. In questo scenario WMI non è necessario per eliminare le notifiche che segnalano solo le modifiche del destinatario.

Nell'esempio di codice MOF seguente vengono descritte le istanze che possono essere usate per registrare un provider di proprietà.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> Solo gli amministratori possono registrare o eliminare un provider di proprietà creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) [**\_ \_ e PropertyProviderRegistration.**](--propertyproviderregistration.md)

 

 

 



