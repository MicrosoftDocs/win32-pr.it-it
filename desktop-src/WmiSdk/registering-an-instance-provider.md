---
description: Per creare un provider di istanze WMI, è necessario registrare l' \_ \_ istanza di Win32Provider che rappresenta il provider utilizzando un'istanza di \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrazione di un provider di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528501"
---
# <a name="registering-an-instance-provider"></a>Registrazione di un provider di istanze

Per creare un [*provider di istanze*](gloss-i.md) WMI, è necessario registrare l'istanza di [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta il provider utilizzando un'istanza di [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Come oggetto COM, il provider deve eseguire la registrazione con il sistema operativo e WMI. Nella procedura seguente si presuppone che il processo di registrazione sia già stato implementato come descritto in [registrazione di un provider](registering-a-provider.md).

Nella procedura riportata di seguito viene descritto come registrare un provider di istanze.

**Per registrare un provider di istanze**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.
2.  Creare un'istanza della classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) che descrive il set di funzionalità del provider.

    La classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) eredita molte proprietà dalla classe padre [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , che fornisce valori booleani che indicano il supporto per caratteristiche specifiche e una matrice di stringhe per indicare il supporto delle query.

    Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](standard-wmi-qualifiers.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Il qualificatore segnala che WMI deve usare un provider **dinamico** per recuperare le istanze della classe. Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.

Nell'esempio di codice seguente viene descritto come registrare un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



