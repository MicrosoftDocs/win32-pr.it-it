---
title: Prefissi URI
description: Il prefisso dell'URI della risorsa è diverso a seconda del XML Schema che descrive la risorsa.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103873089"
---
# <a name="uri-prefixes"></a>Prefissi URI

Il prefisso dell' [*URI della risorsa*](windows-remote-management-glossary.md) è diverso a seconda del XML Schema che descrive la risorsa.

## <a name="prefixes"></a>Prefissi

Se si accede a una classe [*cim*](windows-remote-management-glossary.md) 2,1, ad esempio file di file [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-datafile), il prefisso dell'URI differisce dal prefisso di una classe CIM 2,9, ad esempio **CIM \_ AdminDomain**. Le classi CIM 2,1 sono documentate nella sezione [classi CIM](/windows/desktop/WmiSdk/cimclas) di Strumentazione gestione Windows (WMI).

La maggior parte delle [classi WMI](/windows/desktop/WmiSdk/wmi-classes) si trova nello spazio dei nomi WMI **\\ CIMV2 radice** . Le classi per il provider Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) si trovano nell' **\\ hardware radice**.

Nell'elenco seguente sono inclusi i prefissi URI delle risorse per questi schemi:

-   Classi WMI o CIM 2,1 nello spazio dei nomi **\\ CIMV2 radice**

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   Classi CIM 2,9 o classi IPMI

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Modalità alternativa per accedere alle classi del provider IPMI

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Per altre informazioni, vedere [URI di risorsa](resource-uris.md) e [stringhe URLPrefix](/windows/desktop/Http/urlprefix-strings). Per ulteriori informazioni sulla generazione di un URI per una classe o un metodo WMI, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).

## <a name="prefix-aliases"></a>Alias di prefisso

Un alias di prefisso è un tasto di scelta rapida che rappresenta il prefisso dell'URI di risorsa lungo. È anche possibile usare gli alias nella riga di comando di **WinRM** . Per visualizzare un elenco di alias disponibili, digitare gli **alias della Guida WinRM**.

Tenere presente che un alias non può essere usato in un riferimento all'endpoint (EPR) quando si specifica un URI di risorsa. Gestione remota Windows non è in grado di espandere l'alias quando è incorporato in XML.

Nell'esempio di codice seguente, l'alias WinRM viene usato in un EPR anziché nell'URI completo della risorsa, ovvero `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . In questo caso, WinRM restituisce un errore che indica che il servizio non è in grado di elaborare la richiesta.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



Di seguito sono elencati gli alias definiti e gli URI delle risorse per i quali sostituiscono.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>WMI
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>CIMV2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>WinRM
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>WSMan
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>Shell
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Gestione remota Windows e WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[URI risorse](resource-uris.md)
</dt> </dl>
