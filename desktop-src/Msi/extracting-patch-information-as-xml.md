---
description: Le informazioni sull'applicabilità e la sequenziazione delle patch restituite dalla funzione MsiExtractPatchXMLData o dal metodo ExtractPatchXMLData sono nel formato di un BLOB XML che contiene gli elementi e gli attributi identificati in questo argomento.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Estrazione delle informazioni sulla patch come XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e1e594d3ff2870ca1aaf87245c537045f95d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130679"
---
# <a name="extracting-patch-information-as-xml"></a><span data-ttu-id="19e5a-103">Estrazione delle informazioni sulla patch come XML</span><span class="sxs-lookup"><span data-stu-id="19e5a-103">Extracting Patch Information as XML</span></span>

<span data-ttu-id="19e5a-104">Le informazioni sull'applicabilità e la sequenziazione delle patch restituite dalla funzione [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) o dal metodo [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) sono nel formato di un BLOB XML che contiene gli elementi e gli attributi identificati in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="19e5a-104">The patch sequencing and applicability information that is returned by the [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) function or the [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) method is in the format of an XML blob that contains the elements and attributes that are identified in this topic.</span></span> <span data-ttu-id="19e5a-105">Il BLOB XML può essere fornito a [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) anziché al file di patch completo.</span><span class="sxs-lookup"><span data-stu-id="19e5a-105">The XML blob can be provided to [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) instead of the full patch file.</span></span>

-   <span data-ttu-id="19e5a-106">L'elemento MsiPatch è il primo elemento del BLOB XML e contiene informazioni sulla patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-106">The MsiPatch element is the top element of the XML blob, and contains information about the patch.</span></span>

    <span data-ttu-id="19e5a-107">L'attributo SchemaVersion specifica la versione della definizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="19e5a-107">The SchemaVersion attribute specifies the version of the schema definition.</span></span> <span data-ttu-id="19e5a-108">Lo schema è specificato da MSIPatchApplicability. xsd e la versione dello schema corrente è 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="19e5a-108">The schema is specified by MSIPatchApplicability.xsd and the current schema version is 1.0.0.0.</span></span> <span data-ttu-id="19e5a-109">Il valore dell'attributo PatchGUID è il codice della patch del GUID per il pacchetto di patch ottenuto dalla proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) nel flusso di informazioni di [Riepilogo](summary-information-stream.md) della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-109">The value of the PatchGUID attribute is the GUID patch code for the patch package obtained from the [**Revision Number Summary**](revision-number-summary.md) Property in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span> <span data-ttu-id="19e5a-110">MinMsiVersion è la versione minima del Windows Installer necessario per installare la patch ottenuta dalla proprietà [**riepilogo Conteggio parole**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="19e5a-110">The MinMsiVersion is the minimum version of the Windows Installer required to install the patch obtained from the [**Word Count Summary**](word-count-summary.md) Property.</span></span>

-   <span data-ttu-id="19e5a-111">L'elemento TargetProduct è un elemento contenitore per informazioni su un'applicazione a cui è destinata una patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-111">The TargetProduct element is a container element for information about an application that a patch targets.</span></span>

    <span data-ttu-id="19e5a-112">Se la patch può essere applicata a più applicazioni, possono essere presenti più elementi TargetProduct.</span><span class="sxs-lookup"><span data-stu-id="19e5a-112">There can be multiple TargetProduct elements if the patch can be applied to multiple applications.</span></span> <span data-ttu-id="19e5a-113">Le informazioni contenute nell'elemento TargetProduct vengono estratte dalle trasformazioni incorporate all'interno della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-113">The information in the TargetProduct element is extracted from transforms that are embedded within the patch.</span></span>

-   <span data-ttu-id="19e5a-114">L'elemento TargetProductCode contiene il valore della proprietà [**ProductCode**](productcode.md) dell'applicazione di destinazione prima che sia stata applicata la patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-114">The TargetProductCode element contains the value of the [**ProductCode**](productcode.md) property of the target application before the patch has been applied.</span></span>

    <span data-ttu-id="19e5a-115">Se la patch può essere applicata a più applicazioni, possono essere presenti più elementi TargetProductCode.</span><span class="sxs-lookup"><span data-stu-id="19e5a-115">There can be multiple TargetProductCode elements if the patch can be applied to multiple applications.</span></span>

-   <span data-ttu-id="19e5a-116">L'elemento UpdatedProductCode contiene il GUID del codice prodotto dell'applicazione di destinazione dopo l'applicazione della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-116">The UpdatedProductCode element contains the product code GUID of the target application after the patch is applied.</span></span>

    <span data-ttu-id="19e5a-117">Questo elemento è presente solo se la patch modifica il valore della proprietà [**ProductCode**](productcode.md) .</span><span class="sxs-lookup"><span data-stu-id="19e5a-117">This element is only present if the patch changes the value of the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="19e5a-118">Una patch che modifica **ProductCode** viene definita [aggiornamento principale](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="19e5a-118">A patch that changes the **ProductCode** is referred to as a [Major Upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="19e5a-119">L'elemento TargetVersion contiene la proprietà [**ProductVersion**](productversion.md) dell'applicazione di destinazione prima dell'applicazione della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-119">The TargetVersion element contains the [**ProductVersion**](productversion.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="19e5a-120">L'elemento UpdateVersion contiene il valore della proprietà [**ProductVersion**](productversion.md) dell'applicazione di destinazione dopo l'applicazione della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-120">The UpdateVersion element contains the value of the [**ProductVersion**](productversion.md) property of the target application after the patch is applied.</span></span>

    <span data-ttu-id="19e5a-121">Questo elemento è presente solo se la patch modifica il valore della proprietà [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="19e5a-121">This element is only present if the patch changes the value of the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="19e5a-122">Il BLOB XML per una patch che implementa un [piccolo aggiornamento](small-updates.md), noto anche come QFE, non includerà questo elemento.</span><span class="sxs-lookup"><span data-stu-id="19e5a-122">The XML blob for a patch that implements a [Small Update](small-updates.md), also referred to as a QFE, will not include this element.</span></span> <span data-ttu-id="19e5a-123">Il BLOB XML per una patch che implementa un aggiornamento secondario, noto anche come Service Pack, includerà questo elemento.</span><span class="sxs-lookup"><span data-stu-id="19e5a-123">The XML blob for a patch that implements a minor upgrade, also referred to as a service pack, will include this element.</span></span>

-   <span data-ttu-id="19e5a-124">L'elemento TargetLanguage contiene il valore della proprietà [**ProductLanguage**](productlanguage.md) dell'applicazione di destinazione prima che sia stata applicata la patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-124">The TargetLanguage element contains the value of the [**ProductLanguage**](productlanguage.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="19e5a-125">L'elemento UpdatedLanguages contiene il valore della proprietà [**ProductLanguage**](productlanguage.md) dopo l'applicazione della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-125">The UpdatedLanguages element contains the value of the [**ProductLanguage**](productlanguage.md) property after the patch has been applied.</span></span>
-   <span data-ttu-id="19e5a-126">L'elemento UpgradeCode contiene il valore della proprietà [**UpgradeCode**](upgradecode.md) dell'applicazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="19e5a-126">The UpgradeCode element contains the value of the [**UpgradeCode**](upgradecode.md) property of the target application.</span></span>
-   <span data-ttu-id="19e5a-127">L'elemento ObsoletedPatch contiene i codici patch (GUID) delle patch specificate come obsolete da questa patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-127">The ObsoletedPatch element contains the patch codes (GUIDs) of the patches that are specified as obsolete by this patch.</span></span>

    <span data-ttu-id="19e5a-128">L'elenco delle patch obsolete viene ottenuto dal [**Riepilogo dei numeri di revisione**](revision-number-summary.md) nel flusso di informazioni di [Riepilogo](summary-information-stream.md) della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-128">The list of obsolete patches is obtained from [**Revision Number Summary**](revision-number-summary.md) in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span>

-   <span data-ttu-id="19e5a-129">L'elemento SequenceData contiene informazioni di sequenziazione delle patch per la patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-129">The SequenceData element contains patch sequencing information for the patch.</span></span>

    <span data-ttu-id="19e5a-130">Nel BLOB XML possono essere presenti più elementi SequenceData.</span><span class="sxs-lookup"><span data-stu-id="19e5a-130">There can be multiple SequenceData elements in the XML blob.</span></span> <span data-ttu-id="19e5a-131">Ogni elemento SequenceData contiene le informazioni contenute in una riga della [tabella MsiPatchSequence](msipatchsequence-table.md) della patch.</span><span class="sxs-lookup"><span data-stu-id="19e5a-131">Each SequenceData element contains the information in one row of the [MsiPatchSequence table](msipatchsequence-table.md) of the patch.</span></span> <span data-ttu-id="19e5a-132">L'elemento SequenceData contiene un sottoelemento ProductCode, Sequence e Attributes per le informazioni nei campi corrispondenti della tabella MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="19e5a-132">The SequenceData element contains a ProductCode, Sequence, and Attributes subelement for the information in the corresponding fields in the MsiPatchSequence table.</span></span> <span data-ttu-id="19e5a-133">Per una descrizione di ogni campo, vedere la sezione relativa alla [tabella MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="19e5a-133">See the [MsiPatchSequence table](msipatchsequence-table.md) section for a description of each field.</span></span>

## <a name="extracting-applicability-information"></a><span data-ttu-id="19e5a-134">Estrazione delle informazioni sull'applicabilità</span><span class="sxs-lookup"><span data-stu-id="19e5a-134">Extracting Applicability Information</span></span>

<span data-ttu-id="19e5a-135">Nell'esempio seguente viene illustrato come estrarre le informazioni sull'applicabilità per una patch di Windows Installer (file con estensione msp) utilizzando [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="19e5a-135">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) using [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span> <span data-ttu-id="19e5a-136">Il BLOB XML estratto è basato sulla definizione dello schema in MSIPatchApplicability. xsd e viene restituito a szXMLData.</span><span class="sxs-lookup"><span data-stu-id="19e5a-136">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned to szXMLData.</span></span>


```C++
#include <windows.h>
#include <msi.h>

#pragma comment( lib, "msi.lib" )

void main()
{
     TCHAR szPatchPath[] = TEXT("c:\\scratch\\RTM-RTMQFE.msp");
    TCHAR* szXMLData = NULL;
    DWORD cchXMLData = 0;

    UINT uiStatus = ERROR_SUCCESS;

    // Determine size of XML blob buffer.
    if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
         /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
    {
        // cchXMLData now includes size of szXMLData in characters not including terminating NULL
        ++cchXMLData;

        szXMLData = new TCHAR[cchXMLData];
        if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
            /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
        {
            //
            // szXMLData now contains the XML patch applicability blob. This could be
            // provided to MsiDetermineApplicablePatches or MsiDeterminePatchSequence in the
            // proper format to evaluate patch applicability.
            //

        }

        delete [] szXMLData;
        szXMLData = NULL;
    }
}
```



<span data-ttu-id="19e5a-137">Nell'esempio seguente viene illustrato come estrarre le informazioni sull'applicabilità per un Windows Installer patch (file con estensione msp) in formato XML.</span><span class="sxs-lookup"><span data-stu-id="19e5a-137">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) in XML form.</span></span> <span data-ttu-id="19e5a-138">Il BLOB XML estratto è basato sulla definizione dello schema in MSIPatchApplicability. xsd e restituito in strPatchXML.</span><span class="sxs-lookup"><span data-stu-id="19e5a-138">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned in strPatchXML.</span></span>

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a><span data-ttu-id="19e5a-139">Definizione dello schema di applicabilità patch</span><span class="sxs-lookup"><span data-stu-id="19e5a-139">Patch Applicability Schema Definition</span></span>

<span data-ttu-id="19e5a-140">Copiare il testo seguente nel blocco note o in un altro editor di testo per creare il file di definizione dello schema per le informazioni sull'applicabilità della patch nel BLOB XML.</span><span class="sxs-lookup"><span data-stu-id="19e5a-140">Copy the following text into Notepad or another text editor to create the schema definition file for the patch applicability information in the XML blob.</span></span> <span data-ttu-id="19e5a-141">Assegnare al file il nome MSIPatchApplicability. XSD.</span><span class="sxs-lookup"><span data-stu-id="19e5a-141">Name this file MSIPatchApplicability.XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema id="Applicability" 
    targetNamespace="https://www.microsoft.com/msi/patch_applicability.xsd" 
    elementFormDefault="qualified" 
    xmlns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:mstns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema">
    
    <xs:element name="MsiPatch">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="TargetProduct" minOccurs="1" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="TargetProductCode" type="ValidateGUID" />
                            <xs:element name="UpdatedProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetVersion" type="ValidateVersion" />
                            <xs:element name="UpdatedVersion" type="Version" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetLanguage" type="ValidateLanguage" />
                            <xs:element name="UpdatedLanguages" type="intList" minOccurs="0" maxOccurs="1" />
                            <xs:element name="UpgradeCode" type="ValidateGUID" />
                            <xs:element name="UpdatedUpgradeCode" type="GUID" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                        <xs:attribute name="MinMsiVersion" type="xs:int" />
                    </xs:complexType>
                </xs:element>
                <xs:element name="TargetProductCode" type="GUID" minOccurs="1" maxOccurs="unbounded" />
                <xs:element name="ObsoletedPatch" minOccurs="0" maxOccurs="unbounded" type="GUID" />
                <xs:element name="SequenceData" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="PatchFamily" type="Identifier" />
                            <xs:element name="ProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="Sequence" type="Version" />
                            <xs:element name="Attributes" type="xs:int" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
            <xs:attribute name="SchemaVersion" type="Version" />
            <xs:attribute name="PatchGUID" type="GUID" />
            <xs:attribute name="MinMsiVersion" type="xs:int" />
            <xs:attribute name="TargetsRTM" type="xs:boolean" use="optional" />
        </xs:complexType>
    </xs:element>
    <xs:simpleType name="GUID">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:simpleType name="Version">
        <xs:restriction base="xs:string">
            <xs:pattern value="[0-9]{1,5}(\.[0-9]{1,5}){0,3}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:complexType name="ValidateGUID">
        <xs:simpleContent>
            <xs:extension base="GUID">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateVersion">
        <xs:simpleContent>
            <xs:extension base="Version">
                <xs:attribute name="ComparisonType">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="LessThan" />
                            <xs:enumeration value="LessThanOrEqual" />
                            <xs:enumeration value="Equal" />
                            <xs:enumeration value="GreaterThanOrEqual" />
                            <xs:enumeration value="GreaterThan" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="ComparisonFilter">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="Major" />
                            <xs:enumeration value="MajorMinor" />
                            <xs:enumeration value="MajorMinorUpdate" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateLanguage">
        <xs:simpleContent>
            <xs:extension base="xs:int">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:simpleType name="intList">
        <xs:list itemType="xs:int" />
    </xs:simpleType>
    <xs:simpleType name="Identifier">
        <xs:restriction base="xs:string">
            <xs:pattern value="[_a-zA-Z][_a-zA-Z0-9\.]*" />
        </xs:restriction>
    </xs:simpleType>
</xs:schema>
```

## <a name="related-topics"></a><span data-ttu-id="19e5a-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19e5a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e5a-143">**ExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="19e5a-143">**ExtractPatchXMLData**</span></span>](installer-extractpatchxmldata.md)
</dt> <dt>

[<span data-ttu-id="19e5a-144">**MsiDeterminePatchSequence**</span><span class="sxs-lookup"><span data-stu-id="19e5a-144">**MsiDeterminePatchSequence**</span></span>](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[<span data-ttu-id="19e5a-145">**MsiDetermineApplicablePatches**</span><span class="sxs-lookup"><span data-stu-id="19e5a-145">**MsiDetermineApplicablePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[<span data-ttu-id="19e5a-146">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="19e5a-146">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



