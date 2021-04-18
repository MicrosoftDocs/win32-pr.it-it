---
description: Prima di implementare il provider, è necessario innanzitutto registrare il provider con WMI. La registrazione del provider definisce il tipo di provider e le classi supportate dal provider. WMI può accedere solo a provider registrati.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrazione di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314579"
---
# <a name="registering-a-provider"></a>Registrazione di un provider

Prima di implementare il provider, è necessario innanzitutto registrare il provider con WMI. La registrazione del provider definisce il tipo di provider e le classi supportate dal provider. WMI può accedere solo a provider registrati.

> [!Note]  
> Per ulteriori informazioni sulla registrazione di un provider MI, vedere [procedura: registrare un provider mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).

 

Prima di registrare il provider, è possibile scrivere il codice del provider. Tuttavia, è molto difficile eseguire il debug di un provider non registrato con WMI. La determinazione delle interfacce per il provider consente inoltre di delineare lo scopo e la struttura di un provider. La registrazione del provider consente pertanto di progettare il provider.

Solo gli amministratori possono registrare o eliminare un provider.

Un provider deve essere registrato per tutti i diversi tipi di funzioni del provider che esegue. Quasi tutti i provider forniscono istanze delle classi che definiscono, ma possono anche fornire dati della proprietà, metodi, eventi o classi. Il provider può inoltre essere registrato come provider di consumer di eventi o provider di contatori delle prestazioni. È consigliabile combinare tutte le funzionalità del provider in un provider anziché avere molti provider distinti per ogni tipo. Un esempio è il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), che fornisce metodi e istanze, e il [provider di quote disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), che fornisce istanze, metodi ed eventi.

Un provider deve essere registrato per tutti i diversi tipi di funzioni del provider che esegue. Quasi tutti i provider forniscono istanze delle classi che definiscono, ma possono anche fornire dati della proprietà, metodi, eventi o classi. Il provider può inoltre essere registrato come provider di consumer di eventi o provider di contatori delle prestazioni.

Per ogni tipo di registrazione viene utilizzata la stessa istanza di [**\_ \_ Win32Provider**](--win32provider.md) :

-   [Registrazione di un provider di istanze](registering-an-instance-provider.md)
-   [Registrazione di un provider di classi](registering-a-class-provider.md)
-   [Registrazione di un provider di metodi](registering-a-method-provider.md)
-   [Registrazione di un provider di eventi](registering-an-event-provider.md)
-   [Registrazione di un provider di consumer di eventi](registering-an-event-consumer-provider.md)
-   [Creazione di un provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Esempio: creazione e registrazione di un'istanza di un provider

Nell'esempio seguente viene illustrato un file MOF che crea e registra un'istanza del [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) nello \\ spazio dei nomi CIMV2 radice. Assegna l'alias $Reg al provider per evitare il lungo percorso necessario nelle registrazioni di istanze e metodi. Per ulteriori informazioni, vedere [creazione di un alias](creating-an-alias.md).

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a>Esempio: registrazione di un provider

Nella procedura riportata di seguito viene descritto come registrare un provider.

**Per registrare un provider**

1.  Registrare il provider come server COM.

    Se necessario, potrebbe essere necessario creare voci del registro di sistema. Questo processo si applica a tutti i server COM e non è correlato a WMI. Per ulteriori informazioni, vedere la sezione COM nella documentazione di Microsoft Windows Software Development Kit (SDK).

2.  Creare un file MOF che contiene istanze di [**\_ \_ Win32Provider**](--win32provider.md) e un'istanza di una classe derivata direttamente o indirettamente da [**\_ \_ ProviderRegistration**](--providerregistration.md), ad esempio [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Solo gli amministratori possono registrare o eliminare un provider creando istanze delle classi derivate da **\_ \_ Win32Provider** o [**\_ \_ ProviderRegistration**](--providerregistration.md).
3.  Impostare [**HostingModel**](--win32provider.md) nell'istanza di **\_ \_ Win32Provider** in base ai valori dei modelli di [hosting](provider-hosting-and-security.md).

    > [!Note]  
    > A meno che il provider non richieda i privilegi elevati dell'account LocalSystem, la proprietà [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) deve essere impostata su "NetworkServiceHost". Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

     

    Nell'esempio MOF seguente dell'esempio completo viene illustrato il codice che crea un'istanza di [**\_ \_ Win32Provider**](--win32provider.md).

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Istanza di una classe derivata direttamente o indirettamente da [**\_ \_ ProviderRegistration**](--providerregistration.md)per descrivere l'implementazione logica del provider. Un provider può essere registrato per diversi tipi di funzionalità. Nell'esempio precedente viene registrato RegProv come istanza e provider di metodi. Tuttavia, se RegProv supporta la funzionalità, può essere registrato anche come proprietà o provider di eventi. Nella tabella seguente sono elencate le classi che registrano la funzionalità del provider.

    

    | Classi di registrazione del provider                                                        | Descrizione                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | Registra un [provider di istanze](registering-an-instance-provider.md).             |
    | [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | Registra un [provider di eventi](registering-an-event-provider.md).                   |
    | [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | Registra un [provider di consumer di eventi](registering-an-event-consumer-provider.md). |
    | [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | Registra un [provider di metodi](registering-an-event-consumer-provider.md).          |
    | [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | Registra un [provider di proprietà](registering-a-property-provider.md).               |

    

     

5.  Inserire il file MOF in una directory permanente.

    In genere, è necessario inserire il file nella directory di installazione del provider.

6.  Compilare il file MOF usando [mofcomp](mofcomp.md) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

    **Windows 8 e Windows Server 2012:** Quando si installano i provider, sia [**mofcomp**](mofcomp.md) che l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) considerano i \[ \] \[ qualificatori chiave e statici \] come true se sono presenti, indipendentemente dai valori effettivi. Altri qualificatori vengono considerati false se sono presenti ma non sono impostati in modo esplicito su true.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> </dl>

 

 
