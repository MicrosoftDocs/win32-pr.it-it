---
title: URI risorse
description: Un URI di risorsa è un identificatore per un tipo distinto di operazione di gestione o valore usato dai servizi di gestione che implementano il WS-Management protocollo.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f13e18abd7ea452b84043dfef3d6bf6b18be6c476c0dfff9a34e42e45dbc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323728"
---
# <a name="resource-uris"></a>URI risorse

Un [*URI di risorsa*](windows-remote-management-glossary.md) è un identificatore per un tipo distinto di operazione di gestione o valore usato dai servizi di gestione che implementano il WS-Management protocollo. Un valore di gestione può essere la temperatura all'interno di un computer. Un esempio di operazione di gestione è l'avvio di un servizio arrestato o l'impostazione di una quota utente del volume del disco.

## <a name="resource-uri-format"></a>Formato URI risorsa

Un URI è costituito da un prefisso e da un percorso a una risorsa, come illustrato nell'esempio seguente:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Questa specifica dello schema indica che l'URI è basato sulla versione 1 del protocollo WS-Management ufficiale e che la risorsa è un [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello spazio dei nomi \\ "cimv2 radice" del repository WMI. I prefissi URI contengono una specifica dello schema, ad esempio "schemas.microsoft.com/wbem/wsman/1/wmi" e un tipo specifico di risorsa, ad esempio **\_ LogicalDisk Win32.** Per altre informazioni sull'identificazione di un'istanza specifica di una classe WMI, vedere Windows [Gestione remota e WMI](windows-remote-management-and-wmi.md).

Per altre informazioni, vedere [Prefissi URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Tipi di URI delle risorse

Sebbene [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) sia l'origine principale dei dati di gestione per i sistemi operativi basati su Windows, esistono anche altre origini dello schema di gestione.

L'elenco seguente descrive diversi tipi di URI di risorsa usati Windows gestione remota:

-   URI WMI

    Questo gruppo di URI [](/windows/desktop/WmiSdk/gloss-c) rappresenta un percorso di Common Information Model che include lo spazio dei nomi e la classe.

    Gli URI WMI possono essere usati in:

    -   [**Metodi di**](session.md) sessione
    -   [**Metodi di IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   [**Metodi WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) o [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   [**Metodi di ResourceLocator**](resourcelocator.md) [**o IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   URI IPMI

    Questo gruppo di URI rappresenta gli URI standard del settore basati su CIM versione 2.9. Gli URI IPMI possono essere usati nei [**metodi di**](session.md) sessione [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).

    Un esempio è https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Questa risorsa viene definita [](https://www.dmtf.org/home) in base allo DMTF.org CIM.

-   URI di configurazione di Gestione remota Windows

    Questo gruppo di URI sono operazioni di configurazione per la configurazione del [*listener*](windows-remote-management-glossary.md) WinRM.

    https://schemas.microsoft.com/wbem/wsman/1/config/listener può essere usato nei [**metodi Di**](session.md) [**sessione Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md)ed [**Enumerate**](session-enumerate.md).

-   URI [*del registro*](windows-remote-management-glossary.md) eventi di sistema (SEL)

    Questo gruppo di URI sottoscrive gli eventi dell'agente di raccolta eventi dal BMC. È possibile sottoscrivere questi eventi usando lo strumento da riga di comando **Wevtutil.** Per altre informazioni, vedere https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Maiuscole/minuscole

Il [*plug-in WMI*](windows-remote-management-glossary.md) mantiene il caso dell'URI della risorsa ricevuto in una richiesta. Tuttavia, per garantire l'interoperabilità con altre implementazioni del protocollo WS-Management, usare il caso corretto per la risorsa richiesta nell'URI della risorsa. La distinzione tra maiuscole e minuscole è l'ortografia definita dal provider di risorse.

Anche se gli URI delle risorse non richiedono la distinzione tra maiuscole e minuscole, [*il frammento*](windows-remote-management-glossary.md) XML lo fa. Un frammento specifica una sola proprietà, anziché l'intero set di proprietà per una risorsa. Nel caso di risorse WMI, la sintassi del frammento ottiene una proprietà da un'istanza di risorsa. Ad esempio, per ottenere solo la **proprietà Version** dal sistema [**operativo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) è necessario usare un frammento. Per altre informazioni sui frammenti, vedere "Aggiunta di un selettore a un oggetto ResourceLocator o IWSManResourceLocator" in Windows Gestione remota [e WMI.](windows-remote-management-and-wmi.md)

Seguendo gli standard XML [*e XPath,*](windows-remote-management-glossary.md) il [*plug-in WMI*](windows-remote-management-glossary.md) applica la distinzione tra maiuscole e minuscole per frammenti e XML che definisce i parametri di input per un metodo. La distinzione tra maiuscole e minuscole è necessaria per supportare lo standard XPath 1.0/Livello 1. Per ottenere dati WMI tramite WinRM, la distinzione tra maiuscole e minuscole indica che i nomi delle classi, delle proprietà e dei metodi WMI devono corrispondere alla distinzione tra maiuscole e minuscole del nome presente nel repository WMI.

Per altre informazioni, vedere [Sintassi XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Esempi di distinzione tra maiuscole e minuscole

Ad esempio, uno script che ottiene la proprietà **SECURITY \_ DESCRIPTOR** da un'istanza della classe del servizio [**\_ Win32**](/windows/desktop/CIMWin32Prov/win32-service) WMI non può usare la maiuscola per i nomi nel percorso del frammento, ma solo l'URI. Il [*plug-in WMI*](windows-remote-management-glossary.md) WinRM restituisce un errore per l'esempio VBScript seguente perché il codice XML XPath fornito per **FragmentPath** non usa la distinzione tra maiuscole e minuscole corretta. Nel repository WMI la classe è digitata come "Servizio \_ Win32".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



La versione seguente dello stesso esempio illustra l'uso corretto di case per la classe del servizio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) e la **proprietà SECURITY \_ DESCRIPTOR.**


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

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Gestione hardware remota](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 