---
description: Utilizzare un manifesto XML per definire i contatori delle prestazioni forniti dal provider.
ms.assetid: fa13d13a-f2e2-4732-8bf7-cb0a0f1d4ed7
title: Schema dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 5c41e9d54e259d6e53453a55cc97f7734ce793fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756584"
---
# <a name="performance-counters-schema"></a><span data-ttu-id="0b92a-103">Schema dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="0b92a-103">Performance Counters Schema</span></span>

<span data-ttu-id="0b92a-104">V2 i provider di dati sulle prestazioni sono supportati in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0b92a-104">V2 performance data providers are supported on Windows Vista or later.</span></span> <span data-ttu-id="0b92a-105">Usano un. File MAN (manifesto di strumentazione XML) per definire il provider, il CounterSet e i contatori.</span><span class="sxs-lookup"><span data-stu-id="0b92a-105">They use a .MAN (XML instrumentation manifest) file to define the provider, the countersets, and the counters.</span></span>

> [!NOTE]
> <span data-ttu-id="0b92a-106">I manifesti di strumentazione possono contenere informazioni sui provider di Event Tracing for Windows (ETW) e sui provider dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0b92a-106">Instrumentation manifests can contain information about both Event Tracing for Windows (ETW) providers and Performance Counter providers.</span></span> <span data-ttu-id="0b92a-107">Per informazioni dettagliate sui manifesti di strumentazione, vedere [schema EventManifest](/windows/desktop/WES/eventmanifestschema-schema) e [scrittura di un manifesto di strumentazione](/windows/desktop/WES/writing-an-instrumentation-manifest).</span><span class="sxs-lookup"><span data-stu-id="0b92a-107">For details on instrumentation manifests see [EventManifest Schema](/windows/desktop/WES/eventmanifestschema-schema) and [Writing an Instrumentation Manifest](/windows/desktop/WES/writing-an-instrumentation-manifest)).</span></span>

<span data-ttu-id="0b92a-108">Questa sezione descrive gli elementi e i tipi seguenti usati nella `counters` sezione di un manifesto di strumentazione:</span><span class="sxs-lookup"><span data-stu-id="0b92a-108">This section describes the following elements and types that you use in the `counters` section of an instrumentation manifest:</span></span>

- [<span data-ttu-id="0b92a-109">Elementi dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="0b92a-109">Performance Counters Elements</span></span>](performance-counters-elements.md)
- [<span data-ttu-id="0b92a-110">Contatori delle prestazioni tipi semplici</span><span class="sxs-lookup"><span data-stu-id="0b92a-110">Performance Counters Simple Types</span></span>](performance-counters-simple-types.md)
- [<span data-ttu-id="0b92a-111">Contatori delle prestazioni tipi complessi</span><span class="sxs-lookup"><span data-stu-id="0b92a-111">Performance Counters Complex Types</span></span>](performance-counters-complex-types.md)

<span data-ttu-id="0b92a-112">Non usare le `localization` sezioni o `stringTable` del manifesto di strumentazione per le stringhe di dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0b92a-112">Do not use the `localization` or `stringTable` sections of the instrumentation manifest for performance data strings.</span></span> <span data-ttu-id="0b92a-113">Specificare invece le stringhe come valori dell'attributo che si sta impostando.</span><span class="sxs-lookup"><span data-stu-id="0b92a-113">Instead, specify the strings as values of the attribute that you are setting.</span></span>

<span data-ttu-id="0b92a-114">Dopo aver creato il manifesto, usare lo strumento [CTRPP](ctrpp.md) per convalidare il manifesto e generare `.h` i file di codice () e di risorse ( `.rc` ) da usare per la compilazione del provider.</span><span class="sxs-lookup"><span data-stu-id="0b92a-114">After creating the manifest, use the [CTRPP](ctrpp.md) tool to validate the manifest and to generate code (`.h`) and resource (`.rc`) files to be used in building your provider.</span></span>

<span data-ttu-id="0b92a-115">Quando si installa l'applicazione, eseguire lo [ strumento diLodCtr.exe](/windows-server/administration/windows-commands/lodctr) con il `/M:` parametro per installare i contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0b92a-115">When installing your application, run the [LodCtr.exe tool](/windows-server/administration/windows-commands/lodctr) with the `/M:` parameter to install your performance counters.</span></span> <span data-ttu-id="0b92a-116">Lo strumento LodCtr.exe registrerà le informazioni necessarie nel registro di sistema in `HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{ProviderGuid}` , incluso il percorso completo del file binario contenente le risorse di tipo stringa per il provider (come specificato nell' `applicationIdentity` attributo del manifesto).</span><span class="sxs-lookup"><span data-stu-id="0b92a-116">The LodCtr.exe tool will record the necessary information into the registry under `HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{ProviderGuid}`, including the full path to the binary containing the string resources for your provider (as specified in the `applicationIdentity` attribute of the manifest).</span></span> <span data-ttu-id="0b92a-117">Per eseguire LodCtr.exe, è necessario disporre dei privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="0b92a-117">You must have administrator privileges to run LodCtr.exe.</span></span> <span data-ttu-id="0b92a-118">Esempio di comando di installazione:</span><span class="sxs-lookup"><span data-stu-id="0b92a-118">Example installation command:</span></span>

<span data-ttu-id="0b92a-119">**LodCtr.exe** /m: "*manifesto*" \[ "*ApplicationIdentityDirectory*"\]</span><span class="sxs-lookup"><span data-stu-id="0b92a-119">**LodCtr.exe** /M:"*manifest*" \["*ApplicationIdentityDirectory*"\]</span></span>

<span data-ttu-id="0b92a-120">Se è necessario aggiornare un contatore, assicurarsi di disinstallare il vecchio contatore usando lo [ strumentoUnlodCtr.exe](/windows-server/administration/windows-commands/unlodctr_1) con i `/G:` `/P:` parametri o.</span><span class="sxs-lookup"><span data-stu-id="0b92a-120">If you need to update a counterset, be sure to uninstall the old counterset using the [UnlodCtr.exe tool](/windows-server/administration/windows-commands/unlodctr_1) with the `/G:` or `/P:` parameters.</span></span> <span data-ttu-id="0b92a-121">Dopo la disinstallazione del vecchio contatore, è possibile installare il contatore dei contatori aggiornato.</span><span class="sxs-lookup"><span data-stu-id="0b92a-121">After the old counterset is uninstalled, you can install the updated counterset.</span></span>

## <a name="schema"></a><span data-ttu-id="0b92a-122">SCHEMA</span><span class="sxs-lookup"><span data-stu-id="0b92a-122">Schema</span></span>

<span data-ttu-id="0b92a-123">Di seguito è riportato lo schema dei contatori delle prestazioni che è possibile usare per convalidare la `counters` sezione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="0b92a-123">The following is the performance counters schema that you can use to validate the `counters` section of your manifest.</span></span> <span data-ttu-id="0b92a-124">Questo schema si trova nel Windows SDK come `counterman.xsd` .</span><span class="sxs-lookup"><span data-stu-id="0b92a-124">This schema is found in the Windows SDK as `counterman.xsd`.</span></span> <span data-ttu-id="0b92a-125">Per informazioni dettagliate sullo schema usato per convalidare la sezione Strumentazione del manifesto, vedere [schema EventManifest](/windows/desktop/WES/eventmanifestschema-schema).</span><span class="sxs-lookup"><span data-stu-id="0b92a-125">For details on the schema that you use to validate the instrumentation section of the manifest, see [EventManifest Schema](/windows/desktop/WES/eventmanifestschema-schema).</span></span>

``` syntax
<xs:schema
  targetNamespace="http://schemas.microsoft.com/win/2005/12/counters"
  elementFormDefault="qualified"
  xmlns:man="http://schemas.microsoft.com/win/2005/12/counters"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="HexInt32Type">
    <xs:annotation>
      <xs:documentation>Hex 1-8 digits in size</xs:documentation>
    </xs:annotation>
    <xs:restriction base="xs:string">
      <xs:pattern value="0[xX][0-9A-Fa-f]{1,8}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="UInt32Type">
    <xs:annotation>
      <xs:documentation>Hex 1-8 digits in size or unsignedInt</xs:documentation>
    </xs:annotation>
    <xs:union memberTypes="xs:unsignedInt man:HexInt32Type"/>
  </xs:simpleType>

  <xs:simpleType name="CSymbolType">
    <xs:annotation>
      <xs:documentation>A Valid C Symbol or an empty string</xs:documentation>
    </xs:annotation>
    <xs:restriction base="xs:string">
      <xs:pattern value="()|([_a-zA-Z][_0-9a-zA-Z]*)"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="struct">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="name" type="man:CSymbolType" use="required"/>
        <xs:attribute name="type" type="man:CSymbolType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="structs">
    <xs:choice minOccurs="1" maxOccurs="unbounded">
      <xs:element name="struct" type="man:struct"/>
    </xs:choice>
  </xs:complexType>
  
  <xs:complexType name="counterAttribute">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="name" use="required">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="reference"/>
              <xs:enumeration value="noDisplay"/>
              <xs:enumeration value="noDigitGrouping"/>
              <xs:enumeration value="displayAsHex"/>
              <xs:enumeration value="displayAsReal"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:attribute>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  
  <xs:complexType name="counterAttributes">
    <xs:choice minOccurs="1" maxOccurs="5">
      <xs:element name="counterAttribute" type="man:counterAttribute"/>
    </xs:choice>
  </xs:complexType>
  
  <xs:complexType name="counter">
    <xs:choice minOccurs="0" maxOccurs="1">
      <xs:element name="counterAttributes" type="man:counterAttributes">
        <xs:key name="uniqueCounterAttributeName">
          <xs:annotation>
            <xs:documentation>
              Only five counterAttribute elements allowed, they should all be unique.
            </xs:documentation>
          </xs:annotation>
          <xs:selector xpath="./man:counterAttribute"/>
          <xs:field xpath="@name"/>
        </xs:key>
      </xs:element>
    </xs:choice>
    <xs:attribute name="symbol" type="man:CSymbolType" use="optional"/>
    <xs:attribute name="id" type="man:UInt32Type" use="required"/>
    <xs:attribute name="uri" type="xs:anyURI" use="required"/>
    <xs:attribute name="name" use="optional">
      <xs:annotation>
        <xs:documentation>
            This attribute is required for schemaVersion >= 2.0.
        </xs:documentation>
      </xs:annotation>
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:maxLength value="1023"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="nameID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the name string. This attribute is required
            for schemaVersion >= 2.0. It is not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="description" type="xs:string" use="optional">
      <xs:annotation>
        <xs:documentation>
            This attribute is required for schemaVersion >= 2.0.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="descriptionID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the description string. This attribute is required
            for schemaVersion >= 2.0. It is not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="type" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="perf_counter_counter"/>
          <xs:enumeration value="perf_counter_timer"/>
          <xs:enumeration value="perf_counter_queuelen_type"/>
          <xs:enumeration value="perf_counter_large_queuelen_type"/>
          <xs:enumeration value="perf_counter_100ns_queuelen_type"/>
          <xs:enumeration value="perf_counter_obj_time_queuelen_type"/>
          <xs:enumeration value="perf_counter_bulk_count"/>
          <xs:enumeration value="perf_counter_text"/>
          <xs:enumeration value="perf_counter_rawcount"/>
          <xs:enumeration value="perf_counter_large_rawcount"/>
          <xs:enumeration value="perf_counter_rawcount_hex"/>
          <xs:enumeration value="perf_counter_large_rawcount_hex"/>
          <xs:enumeration value="perf_sample_fraction"/>
          <xs:enumeration value="perf_sample_counter"/>
          <xs:enumeration value="perf_counter_timer_inv"/>
          <xs:enumeration value="perf_sample_base"/>
          <xs:enumeration value="perf_average_timer"/>
          <xs:enumeration value="perf_average_base"/>
          <xs:enumeration value="perf_average_bulk"/>
          <xs:enumeration value="perf_obj_time_timer"/>
          <xs:enumeration value="perf_100nsec_timer"/>
          <xs:enumeration value="perf_100nsec_timer_inv"/>
          <xs:enumeration value="perf_counter_multi_timer"/>
          <xs:enumeration value="perf_counter_multi_timer_inv"/>
          <xs:enumeration value="perf_counter_multi_base"/>
          <xs:enumeration value="perf_100nsec_multi_timer"/>
          <xs:enumeration value="perf_100nsec_multi_timer_inv"/>
          <xs:enumeration value="perf_raw_fraction"/>
          <xs:enumeration value="perf_large_raw_fraction"/>
          <xs:enumeration value="perf_raw_base"/>
          <xs:enumeration value="perf_large_raw_base"/>
          <xs:enumeration value="perf_elapsed_time"/>
          <xs:enumeration value="perf_counter_delta"/>
          <xs:enumeration value="perf_counter_large_delta"/>
          <xs:enumeration value="perf_precision_system_timer"/>
          <xs:enumeration value="perf_precision_100ns_timer"/>
          <xs:enumeration value="perf_precision_object_timer"/>
          <xs:enumeration value="perf_counter_composite"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="detailLevel" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="standard"/>
          <xs:enumeration value="advanced"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale" use="optional" default="0">
      <xs:simpleType>
        <xs:restriction base="xs:integer">
          <xs:minInclusive value="-10"/>
          <xs:maxInclusive value="10"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate" use="optional">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="sum"/>
          <xs:enumeration value="avg"/>
          <xs:enumeration value="max"/>
          <xs:enumeration value="min"/>
          <xs:enumeration value="undefined"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="perfFreqID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="multiCounterID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="struct" type="man:CSymbolType" use="optional">
      <xs:annotation>
        <xs:documentation>
          If providerType=userMode, required.
          If providerType=kernelMode, not allowed.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="field" type="man:CSymbolType" use="optional">
      <xs:annotation>
        <xs:documentation>
          If providerType=userMode, required.
          If providerType=kernelMode, not allowed.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
  </xs:complexType>

  <xs:complexType name="counterSet">
    <xs:sequence>
      <xs:element name="structs" type="man:structs" minOccurs="0" maxOccurs="1">
        <xs:annotation>
          <xs:documentation>
            If providerType=userMode, required.
            If providerType=kernelMode, not allowed.
          </xs:documentation>
        </xs:annotation>
      </xs:element>
      <xs:element name="counter" type="man:counter" minOccurs="1" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="symbol" type="man:CSymbolType" use="required"/>
    <xs:attribute name="guid" type="man:GUIDType" use="required"/>
    <xs:attribute name="uri" type="xs:anyURI" use="required"/>
    <xs:attribute name="name" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:maxLength value="1023"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="nameID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the name string. This attribute is required
            for schemaVersion >= 2.0, and not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="description" use="required"/>
    <xs:attribute name="descriptionID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the description string. This attribute is required
            for schemaVersion >= 2.0, and not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="instances" use="optional" default="single">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="single"/>
          <xs:enumeration value="multiple"/>
          <xs:enumeration value="globalAggregate"/>
          <xs:enumeration value="multipleAggregate"/>
          <xs:enumeration value="globalAggregateHistory"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="provider">
    <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="counterSet" type="man:counterSet"/>
    </xs:choice>
    <xs:attribute name="symbol" type="man:CSymbolType" use="optional">
      <xs:annotation>
        <xs:documentation>
          Provider Symbol is required for User Mode providers.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="callback" use="optional" default="default">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="custom"/>
          <xs:enumeration value="default"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid" type="man:GUIDType" use="required"/>
    <xs:attribute name="applicationIdentity" type="xs:string" use="required"/>
    <xs:attribute name="providerType" use="optional" default="userMode">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="userMode"/>
          <xs:enumeration value="kernelMode"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName" type="xs:string" use="optional" default="Counters"/>
    <xs:attribute name="resourceBase" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            This attribute is not allowed for schemaVersion >= 2.0.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="counters">
    <xs:choice minOccurs="1" maxOccurs="1">
      <xs:element name="provider" type="man:provider"/>
    </xs:choice>
    <xs:attribute name="schemaVersion" type="xs:string" use="required"/>
  </xs:complexType>
  
  <xs:element name="counters" type="man:counters">
    <xs:key name="uniqueCounterSetGUID">
      <xs:annotation>
        <xs:documentation>
          Counter Set GUID should be unique across the entire document. The
          counter set registration fails if the GUID is already registered.
          To update a counter set that is registered, you must first
          uninstall the counter set and register it again.
        </xs:documentation>
      </xs:annotation>
      <xs:selector xpath="./man:provider/man:counterSet"/>
      <xs:field xpath="@guid"/>
    </xs:key>
  </xs:element>
  
</xs:schema>
```

## <a name="example-user-mode-manifest"></a><span data-ttu-id="0b92a-126">Manifesto User-Mode di esempio</span><span class="sxs-lookup"><span data-stu-id="0b92a-126">Example User-Mode Manifest</span></span>

<span data-ttu-id="0b92a-127">Di seguito viene illustrato un manifesto di esempio che definisce i contatori delle prestazioni per un provider in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="0b92a-127">The following shows an example manifest that defines performance counters for a user-mode provider.</span></span>

```XML
<?xml version="1.0"?>
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    >

  <instrumentation>

    <counters
      xmlns="http://schemas.microsoft.com/win/2005/12/counters"
      schemaVersion="2.0">

      <provider
        callback="custom"
        applicationIdentity="myprovider.exe"
        symbol="MY_PROVIDER"
        providerType="userMode"
        providerGuid="{ab8e1320-965a-4cf9-9c07-fe25378c2a23}">

        <counterSet
          guid="{dd36a036-c923-4794-b696-70577630b5cf}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1"
          symbol="MY_LOGICALDISK"
          name="My LogicalDisk"
          nameID="100"
          description="This is a sample counter set with multiple instances."
          descriptionID="102"
          instances="multiple">

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter1"
            symbol="MY_LOGICALDISK_FREE_MB"
            name="My Free Megabytes"
            nameID="104"
            description="First sample counter."
            descriptionID="106"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1"
            />

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter2"
            symbol="MY_LOGICALDISK_SEC_PER_TRANSFER"
            name="My Avg. Disk sec/Transfer"
            nameID="108"
            description="Second sample counter."
            descriptionID="110"
            type="perf_average_timer"
            baseID="3"
            detailLevel="advanced"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="reference" />
              <counterAttribute name="displayAsReal" />
            </counterAttributes>
          </counter>

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter3"
            symbol="MY_LOGICALDISK_TRANSFER_COUNT"
            type="perf_average_base"
            detailLevel="advanced">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>

        <counterSet
          guid="{f72fdf55-eaa6-45ba-bf6d-4c7cb0d6ef73}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2"
          symbol="MY_SYSTEMOBJECTS"
          name="My System Objects"
          nameID="120"
          description="My System Objects Help."
          descriptionID="122"
          instances="single">

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter1"
            symbol="MY_SYSTEMOBJECTS_PROCESS_COUNT"
            name="Process Count"
            nameID="124"
            description="Process Count Help."
            descriptionID="126"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="noDigitGrouping" />
              <counterAttribute name="displayAsHex" />
            </counterAttributes>
          </counter>

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter2"
            symbol="MY_SYSTEMOBJECTS_THREAD_COUNT"
            name="Thread Count"
            nameID="128"
            description="Thread Count Help."
            descriptionID="130"
            type="perf_counter_rawcount"
            detailLevel="standard"
            />

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter3"
            symbol="MY_SYSTEMOBJECTS_ELAPSED_TIME"
            name="System Elapsed Time"
            nameID="132"
            description="System Elapsed Time Help."
            descriptionID="134"
            type="perf_elapsed_time"
            detailLevel="advanced"
            perfTimeID="4"
            perfFreqID="5"
            defaultScale="1"
            />

          <counter
            id="4"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter4"
            symbol="MY_SYSTEMOBJECTS_PERFTIME"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

          <counter
            id="5"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter5"
            symbol="MY_SYSTEMOBJECTS_PERFFREQ"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>
      </provider>
    </counters>
  </instrumentation>
</instrumentationManifest>
```

## <a name="example-kernel-mode-manifest"></a><span data-ttu-id="0b92a-128">Manifesto Kernel-Mode di esempio</span><span class="sxs-lookup"><span data-stu-id="0b92a-128">Example Kernel-Mode Manifest</span></span>

<span data-ttu-id="0b92a-129">Di seguito viene illustrato un manifesto di esempio che definisce i contatori delle prestazioni per un provider in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="0b92a-129">The following shows an example manifest that defines performance counters for a kernel-mode provider.</span></span>

```XML
<?xml version="1.0"?>
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    >

  <instrumentation>

    <counters
      xmlns="http://schemas.microsoft.com/win/2005/12/counters"
      schemaVersion="2.0">

      <provider
        applicationIdentity="myprovider.exe"
        providerType="kernelMode"
        providerGuid="{ab8e1320-965a-4cf9-9c07-fe25378c2a23}">

        <counterSet
          guid="{dd36a036-c923-4794-b696-70577630b5cf}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1"
          symbol="MY_LOGICALDISK"
          name="My LogicalDisk"
          nameID="100"
          description="This is a sample counter set with multiple instances."
          descriptionID="102"
          instances="multiple">

          <structs>
            <struct name="LogicalDiskData" type="MY_LOGICALDISK_DATA" />
          </structs>

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter1"
            field="FreeMegabytes"
            name="My Free Megabytes"
            nameID="104"
            description="First sample counter."
            descriptionID="106"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1"
            />

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter2"
            field="TransferTime"
            name="My Avg. Disk sec/Transfer"
            nameID="108"
            description="Second sample counter."
            descriptionID="110"
            type="perf_average_timer"
            baseID="3"
            detailLevel="advanced"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="reference" />
              <counterAttribute name="displayAsReal" />
            </counterAttributes>
          </counter>

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter3"
            field="TransferCount"
            type="perf_average_base"
            detailLevel="advanced">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>

        <counterSet
          guid="{f72fdf55-eaa6-45ba-bf6d-4c7cb0d6ef73}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2"
          symbol="MY_SYSTEMOBJECTS"
          name="My System Objects"
          nameID="120"
          description="My System Objects Help."
          descriptionID="122"
          instances="single">

          <structs>
            <struct name="SystemObjectsData" type="MY_SYSTEMOBJECTS_DATA" />
          </structs>

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter1"
            field="ProcessCount"
            name="Process Count"
            nameID="124"
            description="Process Count Help."
            descriptionID="126"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="noDigitGrouping" />
              <counterAttribute name="displayAsHex" />
            </counterAttributes>
          </counter>

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter2"
            field="ThreadCount"
            name="Thread Count"
            nameID="128"
            description="Thread Count Help."
            descriptionID="130"
            type="perf_counter_rawcount"
            detailLevel="standard"
            />

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter3"
            field="SystemElapsedTime"
            name="System Elapsed Time"
            nameID="132"
            description="System Elapsed Time Help."
            descriptionID="134"
            type="perf_elapsed_time"
            detailLevel="advanced"
            perfTimeID="4"
            perfFreqID="5"
            defaultScale="1"
            />

          <counter
            id="4"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter4"
            field="PerfTime"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

          <counter
            id="5"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter5"
            field="PerfFreq"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>
      </provider>
    </counters>
  </instrumentation>
</instrumentationManifest>
```
