---
description: Analogamente ad altri provider di istanze, è possibile registrare un provider a prestazioni elevate con Microsoft Windows&\# 160; Strumentazione gestione (WMI) creando un'istanza delle \_ \_ classi Win32Provider e \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrazione di un provider di High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049759"
---
# <a name="registering-a-high-performance-provider"></a>Registrazione di un provider di High-Performance

Analogamente ad altri provider di istanze, è possibile registrare un provider a prestazioni elevate con Microsoft Strumentazione gestione Windows (WMI) creando un'istanza delle classi [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) . L'istanza **\_ \_ Win32Provider** definisce l'implementazione fisica del provider e l'istanza di **\_ \_ InstanceProviderRegistration** definisce il set di funzionalità del provider. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).

Nella procedura riportata di seguito viene descritto come registrare un provider di istanze a prestazioni elevate.

**Per registrare un provider di istanze a prestazioni elevate**

1.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) che descrive il provider.

    Assicurarsi di aggiungere una proprietà **ClientLoadableCLSID** all'istanza di [**\_ \_ Win32Provider**](--win32provider.md) . Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID** come identificatore di classe. Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI. WMI inoltre utilizza **ClientLoadableCLSID** per supportare le operazioni di aggiornamento.

2.  Creare un'istanza della classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) che descrive il set di funzionalità del provider.

    Assicurarsi di contrassegnare la classe con i qualificatori [**dinamici**](dynamic-qualifier.md) e del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Il qualificatore **dinamico** segnala che WMI deve usare un provider per recuperare le istanze della classe. Il qualificatore del **provider** specifica il nome del provider che WMI deve utilizzare.

    Un provider a prestazioni elevate deve inoltre supportare lo stato del supporto per operazioni, operazioni di enumerazione o entrambi. Assicurarsi di usare le proprietà **SupportsGet** e **SupportsEnumeration** nell'implementazione.

Nell'esempio di codice seguente viene illustrato come implementare le classi [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) per un provider a prestazioni elevate.

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



