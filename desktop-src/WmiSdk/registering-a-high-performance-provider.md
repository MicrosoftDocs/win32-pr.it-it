---
description: Come altri provider di istanze, si registra un provider a prestazioni elevate con Microsoft Windows&\# 160; Strumentazione gestione (WMI) creando un'istanza \_ \_ delle classi Win32Provider \_ \_ e InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrazione di un provider High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ee52db95290810a046d23781dbccf666cd63a19b01bf9414b2e224b8137f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992571"
---
# <a name="registering-a-high-performance-provider"></a>Registrazione di un provider High-Performance

Analogamente ad altri provider di istanze, è possibile registrare un provider a prestazioni elevate con Strumentazione gestione Microsoft Windows (WMI) creando un'istanza delle [**\_ \_ classi Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration.**](--instanceproviderregistration.md) **\_ \_ L'istanza Win32Provider** definisce l'implementazione fisica del provider e **\_ \_ l'istanza InstanceProviderRegistration** definisce il set di funzionalità del provider. Per altre informazioni, vedere [Registrazione di un provider.](registering-a-provider.md)

Nella procedura seguente viene descritto come registrare un provider di istanze a prestazioni elevate.

**Per registrare un provider di istanze ad alte prestazioni**

1.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) che descrive il provider.

    Assicurarsi di aggiungere una **proprietà ClientLoadableCLSID** all'istanza [**\_ \_ win32Provider.**](--win32provider.md) Se il provider e il client si trovano nello stesso computer, WMI carica il provider in-process nel client usando **ClientLoadableCLSID come** identificatore di classe. Quando il provider e il client si trovano in computer diversi, WMI carica il provider in-process in WMI. WMI usa anche **ClientLoadableCLSID per** supportare le operazioni di aggiornamento.

2.  Creare un'istanza della [**\_ \_ classe InstanceProviderRegistration**](--instanceproviderregistration.md) che descrive il set di funzionalità del provider.

    Assicurarsi di contrassegnare la classe con entrambi i [**qualificatori Dynamic**](dynamic-qualifier.md) [**e Provider.**](/windows/desktop/api/Provider/nl-provider-provider) Il **qualificatore dinamico** segnala che WMI deve utilizzare un provider per recuperare le istanze della classe. Il **qualificatore** Provider specifica il nome del provider che WMI deve utilizzare.

    Un provider a prestazioni elevate deve anche specificare il supporto per operazioni, operazioni di enumerazione o entrambe. Assicurarsi di usare le proprietà **SupportsGet** **e SupportsEnumeration** nell'implementazione.

L'esempio di codice seguente illustra come implementare le [**\_ \_ classi Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) per un provider ad alte prestazioni.

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

[Creazione di un provider di istanze in un provider High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



