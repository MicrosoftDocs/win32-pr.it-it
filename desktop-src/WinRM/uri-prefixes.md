---
title: Prefissi URI
description: Il prefisso URI della risorsa è diverso a seconda dello schema XML che descrive la risorsa.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b44744d7ac7d158bd7d00423396681fef1499c94d61b5cb74a1dee48dad5c784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898671"
---
# <a name="uri-prefixes"></a>Prefissi URI

Il [*prefisso URI della*](windows-remote-management-glossary.md) risorsa è diverso a seconda dello schema XML che descrive la risorsa.

## <a name="prefixes"></a>Prefissi

Se si accede a una classe [*CIM*](windows-remote-management-glossary.md) 2.1, ad esempio [**CIM \_ DataFile,**](/windows/desktop/CIMWin32Prov/cim-datafile)il prefisso dell'URI è diverso dal prefisso per una classe CIM 2.9, ad esempio **CIM \_ AdminDomain.** Le classi CIM 2.1 sono documentate nella sezione [Classi CIM](/windows/desktop/WmiSdk/cimclas) di Windows Management Instrumentation (WMI).

La [maggior parte delle classi WMI](/windows/desktop/WmiSdk/wmi-classes) è nello spazio dei nomi WMI **\\ cimv2** radice. Le classi per il provider [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)(Microsoft Intelligent Platform Management Interface) sono **\\ nell'hardware radice.**

L'elenco seguente contiene i prefissi URI delle risorse per questi schemi:

-   Classi WMI o CIM 2.1 nello spazio **dei \\ nomi radice cimv2**

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   Classi CIM 2.9 o classi IPMI

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Modalità alternativa per accedere alle classi del provider IPMI

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Per altre informazioni, vedere [URI delle risorse e](resource-uris.md) stringhe [UrlPrefix.](/windows/desktop/Http/urlprefix-strings) Per altre informazioni sulla generazione di un URI per una classe o un metodo WMI, Windows [gestione remota e WMI.](windows-remote-management-and-wmi.md)

## <a name="prefix-aliases"></a>Alias di prefisso

Un alias di prefisso è un collegamento che rappresenta il prefisso URI di risorsa lungo. È anche possibile usare gli alias nella **riga di comando di Winrm.** Per visualizzare un elenco degli alias disponibili, digitare **Winrm help aliases**.

Tenere presente che non è possibile usare un alias all'interno di un riferimento all'endpoint (EPR) quando si specifica un URI di risorsa. Windows Gestione remota non è in grado di espandere l'alias quando è incorporato in XML.

Nell'esempio di codice seguente l'alias winrm viene usato in una EPR anziché nell'URI completo della risorsa, ovvero `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . In questo caso, WinRM restituisce un errore che indica che il servizio non è in grado di elaborare la richiesta.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



Di seguito sono elencati gli alias definiti e gli URI delle risorse per i quali vengono sostituiti.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>Wmi
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>cimv2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>Winrm
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>wsman
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>Guscio
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Windows Gestione remota e WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[URI risorse](resource-uris.md)
</dt> </dl>
