---
title: Gestione remota Windows e WMI
description: Gestione remota Windows può essere utilizzato per recuperare i dati esposti da Strumentazione gestione Windows.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321098"
---
# <a name="windows-remote-management-and-wmi"></a>Gestione remota Windows e WMI

Gestione remota Windows può essere utilizzato per recuperare i dati esposti da Strumentazione gestione Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page) e [mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)). È possibile ottenere dati WMI con script o applicazioni che utilizzano l' [API di scripting WinRM](winrm-scripting-api.md) o tramite lo strumento da riga di comando **WinRM** .

WinRM supporta la maggior parte delle classi e delle operazioni WMI note, inclusi gli oggetti incorporati. WinRM può utilizzare WMI per raccogliere dati sulle [*risorse*](windows-remote-management-glossary.md) o per gestire le risorse in un sistema operativo basato su Windows. Ciò significa che è possibile ottenere dati su oggetti quali dischi, schede di rete, servizi o processi nell'azienda tramite il set di [classi WMI](/windows/desktop/WmiSdk/wmi-classes)esistente. È inoltre possibile accedere ai dati hardware disponibili dal [provider standard IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)di WMI.

## <a name="identifying-a-wmi-resource"></a>Identificazione di una risorsa WMI

È possibile fare riferimento a una classe WMI come [*risorsa*](windows-remote-management-glossary.md) in WinRM e nel protocollo WS-Management: un tipo di entità gestita, ad esempio un servizio o un disco.

Una classe o un metodo WMI viene identificato da un [*URI*](windows-remote-management-glossary.md), come qualsiasi altra risorsa quando si usa il protocollo WS-Management. L'URI può specificare una risorsa WMI (classe), un'azione WMI (metodo) o identificare un'istanza specifica di una classe nei [*messaggi*](windows-remote-management-glossary.md) inviati in rete. Per altre informazioni, vedere [URI di risorsa](resource-uris.md).

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Costruzione del prefisso URI per le classi WMI

Il prefisso URI contiene una parte fissa e lo spazio dei nomi WMI. Ad esempio, il prefisso URI in Windows Server che contiene la parte fissa del prefisso è: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Ciò consente di generare il prefisso URI per qualsiasi spazio dei nomi WMI. Ad esempio, per accedere allo spazio dei nomi WMI **\\ predefinito radice** , usare il prefisso URI seguente: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

La maggior parte delle classi WMI per la gestione si trova nello spazio dei nomi **\\ CIMV2 radice** . Per accedere alle classi e alle istanze nello spazio dei nomi **\\ CIMV2 radice** , usare il prefisso URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Per altre informazioni, vedere [URI di risorsa](resource-uris.md).

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Generazione di un URI completo per le classi WMI

L'URI fornito, sia per lo strumento da riga di comando **WinRM** che per uno script, è costituito dal prefisso e dalla specifica della risorsa.

Nella procedura seguente viene descritto come generare un URI di risorsa per ottenere una classe WMI o per utilizzarla in un'operazione di enumerazione.

**Per generare un URI di risorsa per una classe WMI**

1.  Iniziare con il prefisso che indica che è necessario utilizzare lo schema del protocollo WS-Management.

    https://schemas.microsoft.com/wbem/wsman/1

    Il prefisso dell'URI della risorsa per le classi WMI è sempre lo stesso. Per ulteriori informazioni, vedere [prefissi URI](uri-prefixes.md).

2.  Aggiungere lo spazio dei nomi WMI al prefisso.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Aggiungere il nome della classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Per impostare il valore di una proprietà o per richiamare un metodo specifico, aggiungere il valore o i valori della chiave richiesti per la classe.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Se si lascia vuoto il valore della chiave, non sarà possibile modificare il valore della proprietà originale.

    > [!Note]  
    > Se si lascia vuoto il valore della chiave, il valore della proprietà viene impostato su **null**.

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Individuazione di una risorsa WMI con WinRM

È possibile ottenere dati WMI tramite lo strumento da riga di comando, **WinRM** o tramite uno script Visual Basic che utilizza l' [API di scripting WinRM](winrm-scripting-api.md). Non è possibile usare un [percorso WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) per individuare una risorsa. Al contrario, è possibile convertire lo spazio dei nomi WMI e la gerarchia in un [*URI*](windows-remote-management-glossary.md).

L'URI WinRM per una classe WMI contiene due parti: il [prefisso URI](uri-prefixes.md) e la classe a cui si vuole accedere.

Ad esempio, è possibile fornire l'URI seguente al metodo [**Session. enumerate**](session-enumerate.md) per elencare tutti i servizi in un computer. Il prefisso dell'URI è `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` e la classe è [**il \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

In WMI elencare i dati per tutte le istanze di una risorsa o di una classe in diversi modi:

-   Query per tutte le istanze di tale risorsa.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Una chiamata a [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) o [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

In WinRM è possibile elencare tutte le istanze di una risorsa: [**Session. enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Individuazione di un'istanza specifica di una risorsa WMI

In WMI è possibile designare una particolare istanza di una classe specificando i valori per le proprietà chiave o eseguendo una query per un'istanza che corrisponde a un elenco di valori di proprietà. Le proprietà chiave hanno il [**qualificatore della chiave**](/windows/desktop/WmiSdk/key-qualifier)WMI.

È possibile ottenere un'istanza specifica di una classe in diversi modi:

-   Una chiamata a [**Session. enumerate**](session-enumerate.md) con i parametri *Filter* e *dialetto* per creare una query.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Una chiamata a [**SWbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get). Per [**Session. Get**](session-get.md), è necessario specificare uno o più valori di chiave specifici, preceduti da un punto interrogativo (?).

    Il formato dell'URI per un'istanza specifica è `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Una classe WMI può avere più di una chiave. Le coppie nome/valore chiave sono separate da un segno "+". In tal caso, il formato è: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    La sintassi WinRM per ottenere un oggetto WMI singleton è diversa da WMI. Un singleton è una classe WMI definita in modo che sia consentita una sola istanza. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) o [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) sono esempi di una classe singleton WMI.

    La sintassi WMI per i singleton è illustrata nell'esempio di codice VBScript seguente.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    Nell'esempio seguente viene illustrata la sintassi singleton di WinRM che non utilizza "@".

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Aggiunta di un [*selettore*](windows-remote-management-glossary.md) a un oggetto [**resourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .

    Nell'esempio di codice VBScript riportato di seguito viene illustrato come utilizzare un selettore per ottenere un'istanza specifica del [**\_ processore Win32**](/windows/desktop/CIMWin32Prov/win32-processor).

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Prefissi URI](uri-prefixes.md)
</dt> <dt>

[URI risorse](resource-uris.md)
</dt> <dt>

[Creazione di script in Gestione remota Windows](scripting-in-windows-remote-management.md)
</dt> </dl>
