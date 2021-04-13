---
title: Configurazione del plug-in del servizio WinRM
description: Un plug-in di Gestione remota Windows (WinRM) deve essere registrato nel catalogo WinRM per consentire all'infrastruttura di determinare in modo dinamico il set di plug-in disponibili e gli URI delle risorse supportati.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104339603"
---
# <a name="winrm-service-plug-in-configuration"></a>Configurazione del plug-in del servizio WinRM

Un plug-in di Gestione remota Windows (WinRM) deve essere registrato nel catalogo WinRM per consentire all'infrastruttura di determinare in modo dinamico il set di plug-in disponibili e gli [*URI delle risorse*](windows-remote-management-glossary.md) supportati. Tutti gli [*URI di risorsa*](windows-remote-management-glossary.md) per i plug-in WinRM devono essere conformi al formato definito in RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ). La configurazione viene eseguita tramite il servizio WinRM principale.

Il comando seguente registra una configurazione del plug-in con il servizio WinRM:

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> Il servizio gestione remota Windows deve essere riavviato per esporre i plug-in appena registrati.

La configurazione del plug-in è specificata in XML. Di seguito è riportato un esempio.

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



Nell'elenco seguente vengono descritti in modo più dettagliato gli elementi XML ed è seguito dallo schema di configurazione specificato come XSD.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**
</dt> <dd>

Specifica il nome del file del plug-in per le operazioni. Tutte le variabili di ambiente inserite in questa voce verranno espanse nel contesto degli utenti quando viene ricevuta una richiesta. Ogni utente potrebbe avere una versione diversa della stessa variabile di ambiente, quindi ogni utente potrebbe finire con un plug-in diverso. Questa voce non può essere vuota e deve puntare a un plug-in valido.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nome**
</dt> <dd>

Specifica il nome visualizzato da usare per il plug-in. Se dal plug-in viene restituito un errore, questo nome verrà inserito nel codice XML dell'errore restituito all'applicazione client. Il nome non è specifico delle impostazioni locali.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Architettura** di
</dt> <dd>

Specifica se il plug-in per le operazioni è a 32 bit o a 64 bit. Se questo elemento non viene specificato, il valore predefinito sarà "32" nei sistemi x86 e "64" nei sistemi a 64 bit. Per i sistemi x86, l'unico valore valido è "32". Se il valore è "32" in un sistema a 64 bit, è necessario prendere in considerazione il reindirizzamento WOW64 quando si immettono le informazioni sul **nome del file** . Il file system sottostante userà il reindirizzamento WOW64 per tradurre system32 in SysWow64. Se, ad esempio, **filename** è "% windir% \\ system32 \\myplugin.dll" e **Architecture** è "32", il file del plug-in effettivo si trova in "% windir% \\ SysWow64 \\myplugin.dll".

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**
</dt> <dd>

Configura il formato in cui XML viene passato ai plug-in tramite l'oggetto [**\_ dati WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) . Sono disponibili i tipi seguenti:

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo
</dt> <dd>

I dati XML in arrivo sono contenuti in una \_ \_ struttura di testo del tipo di dati WSMan \_ , che rappresenta l'XML come buffer di memoria **PCWSTR** .

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader
</dt> <dd>

I dati XML in arrivo sono contenuti in un \_ tipo di dati WSMan \_ \_ \_ \_ struttura del Reader WS XML, che rappresenta l'XML come oggetto **XmlReader** , definito nel file di intestazione WebServices. h.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**
</dt> <dd>

Questo nodo è facoltativo e consente a un plug-in di configurare codice XML aggiuntivo che verrà passato al metodo [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup). Questa informazione aggiuntiva non è necessaria per la maggior parte dei plug-in, ma se è necessario usare un plug-in in più scenari che richiedono una semantica di runtime diversa, questo codice XML fornirà la flessibilità necessaria per questa operazione.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Risorse** di
</dt> <dd>

Specifica un elenco di [*URI di risorsa*](windows-remote-management-glossary.md)supportati da questo plug-in. È necessario specificare almeno una voce **resourceUri**. in caso contrario, il codice XML verrà rifiutato.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** di
</dt> <dd>

Rappresenta una singola configurazione [*URI di risorsa*](windows-remote-management-glossary.md).

> [!Note]  
> L'attributo **SupportsOptions** può essere impostato su false. Se **SupportsOptions** è impostato su false, questo attributo non viene elencato quando la risorsa viene enumerata.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** / di **ResourceUri**
</dt> <dd>

Specifica un singolo [*URI di risorsa*](windows-remote-management-glossary.md) in formato completo o come stringa di corrispondenza parziale basata sull'attributo **exactMatch** . Se **exactMatch** non è presente, il valore predefinito è **false**, il che significa che il processore SOAP WinRM eseguirà una corrispondenza parziale all'inizio dell' *URI della risorsa* e, in caso di corrispondenza, lo passerà al plug-in. È possibile specificare l'attributo **SupportsOptions** se all' *URI della risorsa* è consentito passare qualsiasi opzione. Per impostazione predefinita, non sono supportate opzioni e, se presenti nella richiesta client, viene restituito un errore. Se le opzioni sono supportate dal plug-in, è importante che il plug-in restituisca l'errore corretto se è presente un'opzione che il plug-in non riconosce quando il flag **MustUnderstand** è impostato su **true**.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** / di **Funzionalità** di
</dt> <dd>

Specifica una funzionalità disponibile in questo URI di [*risorsa*](windows-remote-management-glossary.md). Sarà presente una voce per ogni tipo di operazione supportata. Sono disponibili le opzioni seguenti:

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Ottieni
</dt> <dd>

Le operazioni get sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** viene usato se l'operazione Get supporta il concetto. L'attributo **SupportFiltering** non è valido e deve essere impostato su false. Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>Mettere
</dt> <dd>

Le operazioni Put sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** viene usato se l'operazione Put supporta il concetto. L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**. Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Creare
</dt> <dd>

Le operazioni di creazione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** viene usato se l'operazione Create supporta il concetto. L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**. Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Eliminare
</dt> <dd>

Le operazioni di eliminazione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** viene usato se l'operazione Delete supporta il concetto. L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**. Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Richiamare
</dt> <dd>

Le operazioni Invoke sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** non è supportato per le operazioni Invoke e deve essere impostato su false. L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**. Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerare
</dt> <dd>

Le operazioni di enumerazione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** non è supportato per le operazioni di enumerazione e deve essere impostato su **false**. L'attributo **SupportFiltering** è valido e se il plug-in supporta il filtro di questo attributo deve essere impostato su **true**. Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Sottoscrivere
</dt> <dd>

Le operazioni di sottoscrizione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** non è supportato per le operazioni di sottoscrizione e deve essere impostato su **false**. L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**. Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell
</dt> <dd>

Le operazioni della shell sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md). L'attributo **SupportFragment** non è supportato per le operazioni della shell e deve essere impostato su **false**. L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**. Questa funzionalità non è valida per un *URI di risorsa* se è supportata anche un'altra funzionalità dell'operazione. Se è configurata una funzionalità di operazione Shell per un *URI di risorsa*, le operazioni get, put, create, DELETE, Invoke ed enumerate vengono elaborate internamente nel servizio WinRM per gestire le shell. Di conseguenza, il plug-in non è in grado di gestire le operazioni.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** / di **Sicurezza**
</dt> <dd>

Questo elemento definisce il descrittore di sicurezza (tramite l'attributo **SDDL** ) da applicare per determinare l'accesso a un [*URI di risorsa*](windows-remote-management-glossary.md) specifico (tramite l'attributo **URI** ). Se **exactMatch** non è presente, l'impostazione predefinita dell'elemento di **sicurezza** è **false**, il che significa che **SDDL** si applica a tutti gli *URI di risorsa* che condividono **URI** come prefisso. Se **exactMatch** è impostato su true, **SDDL** si applica solo all' **URI** esatto specificato. Se sono presenti più voci di **sicurezza** che possono essere applicate a uno specifico *URI di risorsa*, viene usata la corrispondenza del prefisso più lungo per determinare l' **SDDL** appropriato. In seguito alla corrispondenza del prefisso più lungo, se esiste una voce **URI** esatta della corrispondenza, viene sempre scelta come elemento di sicurezza appropriato.

</dd> </dl>

Di seguito è riportato lo schema di configurazione del plug-in specificato come XSD.

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




