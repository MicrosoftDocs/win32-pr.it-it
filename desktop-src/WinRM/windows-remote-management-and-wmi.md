---
title: Windows Gestione remota e WMI
description: Windows La gestione remota può essere usata per recuperare i dati esposti Windows Management Instrumentation.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4d4fab5cd1ee27f664fc43838a62db949c5892147818466edf649641eff203b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642471"
---
# <a name="windows-remote-management-and-wmi"></a>Windows Gestione remota e WMI

Windows La gestione remota può essere usata per recuperare i dati esposti da Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) e [MI).](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) È possibile ottenere dati WMI con script o applicazioni che usano [l'API di scripting WinRM](winrm-scripting-api.md) o tramite lo strumento da riga di comando **Winrm.**

WinRM supporta la maggior parte delle classi e delle operazioni WMI familiari, inclusi gli oggetti incorporati. WinRM può sfruttare WMI per raccogliere dati [*sulle risorse*](windows-remote-management-glossary.md) o per gestire le risorse in un Windows basato su un sistema operativo. Ciò significa che è possibile ottenere dati su oggetti quali dischi, schede di rete, servizi o processi nell'organizzazione tramite il set esistente di [classi WMI](/windows/desktop/WmiSdk/wmi-classes). È anche possibile accedere ai dati hardware disponibili dal [provider IPMI WMI standard.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)

## <a name="identifying-a-wmi-resource"></a>Identificazione di una risorsa WMI

È possibile fare riferimento a una classe WMI come risorsa [*in*](windows-remote-management-glossary.md) WinRM e nel protocollo WS-Management: un tipo di entità gestita, ad esempio un servizio o un disco.

Una classe o un metodo WMI è identificato da un [*URI*](windows-remote-management-glossary.md), esattamente come qualsiasi altra risorsa quando si usa il WS-Management servizio. L'URI può specificare una risorsa WMI (classe), un'azione WMI (metodo) o identificare un'istanza specifica di una classe [*nei*](windows-remote-management-glossary.md) messaggi inviati in rete. Per altre informazioni, vedere [URI delle risorse.](resource-uris.md)

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Costruzione del prefisso URI per le classi WMI

Il prefisso URI contiene una parte fissa e lo spazio dei nomi WMI. Ad esempio, il prefisso URI in Windows Server che contiene la parte fissa del prefisso è: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . In questo modo è possibile generare il prefisso URI per qualsiasi spazio dei nomi WMI. Ad esempio, per accedere allo spazio dei nomi WMI **\\ predefinito** radice, usare il prefisso URI seguente: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

La maggior parte delle classi WMI per la gestione è nello **spazio dei nomi radice \\ cimv2.** Per accedere a classi e istanze nello **spazio dei nomi radice \\ cimv2,** usare il prefisso URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Per altre informazioni, vedere [URI delle risorse.](resource-uris.md)

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Generazione di un URI completo per le classi WMI

L'URI fornito, allo strumento da riga di comando **Winrm** o a uno script, è costituito dal prefisso e dalla specifica della risorsa.

Nella procedura seguente viene descritto come generare un URI di risorsa per ottenere una classe WMI o da utilizzare in un'operazione di enumerazione.

**Per generare un URI di risorsa per una classe WMI**

1.  Iniziare con il prefisso che indica WS-Management schema del protocollo da usare.

    https://schemas.microsoft.com/wbem/wsman/1

    Il prefisso URI della risorsa per le classi WMI è sempre lo stesso. Per altre informazioni, vedere [Prefissi URI.](uri-prefixes.md)

2.  Aggiungere lo spazio dei nomi WMI al prefisso.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Aggiungere il nome della classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Per impostare il valore di una proprietà o per richiamare un metodo specifico, aggiungere il valore o i valori di chiave necessari per la classe .

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Se si lascia vuoto il valore della chiave, non si modificherà il valore originale della proprietà.

    > [!Note]  
    > Se si lascia vuoto il valore della chiave, il valore della proprietà viene impostato su **NULL.**

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Individuazione di una risorsa WMI con WinRM

È possibile ottenere dati WMI tramite lo strumento da riga di comando **Winrm** o tramite uno script Visual Basic che usa l'API di [scripting WinRM](winrm-scripting-api.md). Non si usa un percorso [WMI per](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) individuare una risorsa. Al contrario, si convertono lo spazio dei nomi WMI e la gerarchia in un [*URI*](windows-remote-management-glossary.md).

L'URI winrm per una classe WMI contiene due parti: il prefisso [URI](uri-prefixes.md) e la classe a cui si vuole accedere.

Ad esempio, l'URI seguente può essere fornito al [**metodo Session.Enumerate**](session-enumerate.md) per elencare tutti i servizi in un computer. Il prefisso URI è `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` e la classe è [**Win32 \_ Service.**](/windows/desktop/CIMWin32Prov/win32-service)

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

In WMI elencare i dati per tutte le istanze di una risorsa o di una classe in diversi modi:

-   Query per tutte le istanze di tale risorsa.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Una chiamata a [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) o [**SWbemObject.Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

In WinRM è possibile elencare tutte le istanze di una risorsa: [**Session.Enumerate.**](session-enumerate.md)


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Individuazione di un'istanza specifica di una risorsa WMI

In WMI è possibile designare una particolare istanza di una classe specificando i valori per le proprietà chiave o cercando un'istanza corrispondente a un elenco di valori di proprietà. Le proprietà chiave hanno il [**qualificatore di chiave**](/windows/desktop/WmiSdk/key-qualifier)WMI .

È possibile ottenere un'istanza specifica di una classe in diversi modi:

-   Una chiamata a [**Session.Enumerate con**](session-enumerate.md) i *parametri di* filtro e *dialetto* per creare una query.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Una chiamata a [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get). Per [**Session.Get**](session-get.md)è necessario specificare uno o più valori di chiave specifici, preceduti da un punto interrogativo (?).

    Il formato dell'URI per un'istanza specifica è `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Una classe WMI può avere più di una chiave. Le coppie nome-valore chiave sono separate da un segno "+". In tal caso, il formato è: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    La sintassi di WinRM per ottenere un oggetto WMI singleton è diversa da WMI. Un singleton è una classe WMI definita in modo che sia consentita una sola istanza. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) o [**Win32 \_ WMISetting sono**](/windows/desktop/CIMWin32Prov/win32-wmisetting) esempi di classe singleton WMI.

    La sintassi WMI per i singleton è illustrata nell'esempio di codice VBScript seguente.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    L'esempio seguente illustra la sintassi singleton di WinRM che non usa "@".

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Aggiunta di [*un selettore*](windows-remote-management-glossary.md) a [**un oggetto ResourceLocator**](resourcelocator.md) o [**IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

    Nell'esempio di codice VBScript seguente viene illustrato come usare un selettore per ottenere un'istanza specifica del [**processore Win32. \_**](/windows/desktop/CIMWin32Prov/win32-processor)

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Prefissi URI](uri-prefixes.md)
</dt> <dt>

[URI risorse](resource-uris.md)
</dt> <dt>

[Esecuzione di script Windows gestione remota](scripting-in-windows-remote-management.md)
</dt> </dl>
