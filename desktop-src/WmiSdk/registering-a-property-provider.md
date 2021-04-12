---
description: Per creare un provider di proprietà WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrazione di un provider di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226835"
---
# <a name="registering-a-property-provider"></a>Registrazione di un provider di proprietà

Per creare un [*provider di proprietà*](gloss-p.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md). Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).

Nella procedura riportata di seguito viene descritto come registrare un provider di proprietà.

**Per registrare un provider di proprietà**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider di proprietà.

    La classe [**\_ \_ Win32Provider**](--win32provider.md) accetta i valori predefiniti per altre proprietà, ad esempio il valore **true** per la proprietà **pure** . Per ulteriori informazioni, vedere [**\_ \_ Win32Provider**](--win32provider.md).

2.  Creare un'istanza della classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) che descrive il set di funzionalità del provider.

    La classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , che fornisce valori booleani che indicano il supporto per caratteristiche specifiche e una matrice di stringhe per indicare il supporto delle query.

    Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](dynamic-qualifier.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Il qualificatore **dinamico** segnala che WMI deve usare un provider dinamico per recuperare le istanze della classe che contengono le proprietà supportate. Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.

WMI chiama NewQuery su un provider di eventi quando un consumer client registra una query del filtro eventi che contiene riferimenti a eventi supportati da tale provider di eventi. Il provider di eventi responsabile degli eventi di modifica dell'istanza per la classe EmailClass può quindi essere configurato per generare notifiche solo per il mittente. Quando il provider riceve una query che richiede la notifica delle modifiche apportate alla proprietà Subject, il provider può iniziare a generare tali notifiche. In questo scenario non è necessario che WMI elimini le notifiche che segnalano solo le modifiche del destinatario.

Nell'esempio di codice MOF seguente vengono descritte le istanze di che possono essere utilizzate per registrare un provider di proprietà.

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
> Solo gli amministratori possono registrare o eliminare un provider di proprietà creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).

 

 

 



