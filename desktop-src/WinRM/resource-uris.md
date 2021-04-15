---
title: URI risorse
description: Un URI di risorsa è un identificatore per un tipo distinto di operazione di gestione o di valore utilizzato dai servizi di gestione che implementano il protocollo WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516810"
---
# <a name="resource-uris"></a>URI risorse

Un [*URI di risorsa*](windows-remote-management-glossary.md) è un identificatore per un tipo distinto di operazione di gestione o di valore utilizzato dai servizi di gestione che implementano il protocollo WS-Management. Un valore di gestione potrebbe essere la temperatura all'interno di un computer. Un esempio di operazione di gestione è l'avvio di un servizio interrotto o l'impostazione di una quota utente del volume del disco.

## <a name="resource-uri-format"></a>Formato URI risorsa

Un URI è costituito da un prefisso e da un percorso a una risorsa, come illustrato nell'esempio seguente:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Questa specifica dello schema indica che l'URI è basato sulla versione 1 del protocollo WS-Management ufficiale e che la risorsa è una [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ spazio dei nomi "root cimv2" del repository WMI. I prefissi URI contengono una specifica dello schema, ad esempio "schemas.microsoft.com/wbem/wsman/1/wmi" e un tipo specifico di risorsa, ad esempio **\_ disco logico Win32**. Per ulteriori informazioni sull'identificazione di un'istanza specifica di una classe WMI, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).

Per ulteriori informazioni, vedere [prefissi URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Tipi di URI di risorsa

Sebbene [*Strumentazione gestione Windows (WMI)*](windows-remote-management-glossary.md) sia l'origine principale dei dati di gestione per i sistemi operativi basati su Windows, esistono anche altre origini dello schema di gestione.

L'elenco seguente descrive diversi tipi di URI di risorsa usati da Gestione remota Windows:

-   URI WMI

    Questo gruppo di URI rappresenta un percorso della classe [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) che include lo spazio dei nomi e la classe.

    Gli URI WMI possono essere usati in:

    -   Metodi di [**sessione**](session.md)
    -   Metodi [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   Metodi [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) o [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   Metodi [**resourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   URI IPMI

    Questo gruppo di URI rappresenta gli URI standard del settore basati sulla versione CIM 2,9. Gli URI IPMI possono essere usati nei metodi di [**sessione**](session.md) [**Get**](session-get.md), [**put**](session-put.md), [**enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).

    Un esempio è https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Questa risorsa viene definita in base allo schema CIM [DMTF.org](https://www.dmtf.org/home) .

-   URI di configurazione WinRM

    Questo gruppo di URI è costituito da operazioni di configurazione per la configurazione del [*listener*](windows-remote-management-glossary.md) WinRM.

    https://schemas.microsoft.com/wbem/wsman/1/config/listener può essere usato nei metodi di [**sessione**](session.md) [**Get**](session-get.md), [**put**](session-put.md), [**create**](session-create.md), [**Delete**](session-delete.md)ed [**enumerate**](session-enumerate.md).

-   URI del [*registro eventi di sistema*](windows-remote-management-glossary.md) (SEL)

    Questo gruppo di URI sottoscrive gli eventi dell'agente di raccolta eventi dal BMC. È possibile sottoscrivere questi eventi usando lo strumento da riga di comando **wevtutil** . Per altre informazioni, vedere https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Maiuscole/minuscole

Il [*plug-in WMI*](windows-remote-management-glossary.md) conserva il caso dell'URI della risorsa ricevuto in una richiesta. Tuttavia, per garantire l'interoperabilità con altre implementazioni del protocollo WS-Management, usare il caso corretto per la risorsa richiesta nell'URI della risorsa. Il caso corretto è l'ortografia definita dal provider di risorse.

Sebbene gli URI delle risorse non richiedano la distinzione tra maiuscole e minuscole, il [*frammento*](windows-remote-management-glossary.md) XML Un frammento specifica una sola proprietà, anziché l'intero set di proprietà per una risorsa. Nel caso di risorse WMI, la sintassi del frammento ottiene una proprietà da un'istanza di risorsa. Ad esempio, per ottenere solo la proprietà **Version** da [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) è necessario usare un frammento. Per ulteriori informazioni sui frammenti, vedere "aggiunta di un selettore a un oggetto ResourceLocator o IWSManResourceLocator" in [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).

Secondo gli standard XML e [*XPath*](windows-remote-management-glossary.md) , il [*plug-in WMI*](windows-remote-management-glossary.md) impone la distinzione tra maiuscole e minuscole per i frammenti e il codice XML che definisce i parametri di input per un metodo. La distinzione tra maiuscole e minuscole è necessaria per supportare lo standard XPath 1.0/livello 1. Per ottenere i dati WMI tramite WinRM, la distinzione tra maiuscole e minuscole indica che i nomi delle classi, delle proprietà e dei metodi WMI devono corrispondere al caso del nome trovato nel repository WMI.

Per ulteriori informazioni, vedere [sintassi XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Esempi di distinzione maiuscole/minuscole

Uno script che ottiene la proprietà del **\_ descrittore di sicurezza** da un'istanza della classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) WMI, ad esempio, non può utilizzare il maiuscolo per i nomi nel percorso del frammento, bensì solo l'URI. Il [*plug-in WMI*](windows-remote-management-glossary.md) WinRM restituisce un errore per l'esempio VBScript seguente perché il codice XML XPath fornito per **FragmentPath** non usa la combinazione di maiuscole e minuscole corretta. Nel repository WMI la classe è digitata "servizio Win32 \_ ".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



Nella versione seguente dello stesso esempio viene illustrato l'utilizzo corretto del caso per la classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) e la proprietà del **\_ descrittore di sicurezza** .


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Gestione hardware remota](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 