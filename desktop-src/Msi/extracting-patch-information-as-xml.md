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
# <a name="extracting-patch-information-as-xml"></a>Estrazione delle informazioni sulla patch come XML

Le informazioni sull'applicabilità e la sequenziazione delle patch restituite dalla funzione [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) o dal metodo [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) sono nel formato di un BLOB XML che contiene gli elementi e gli attributi identificati in questo argomento. Il BLOB XML può essere fornito a [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) anziché al file di patch completo.

-   L'elemento MsiPatch è il primo elemento del BLOB XML e contiene informazioni sulla patch.

    L'attributo SchemaVersion specifica la versione della definizione dello schema. Lo schema è specificato da MSIPatchApplicability. xsd e la versione dello schema corrente è 1.0.0.0. Il valore dell'attributo PatchGUID è il codice della patch del GUID per il pacchetto di patch ottenuto dalla proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) nel flusso di informazioni di [Riepilogo](summary-information-stream.md) della patch. MinMsiVersion è la versione minima del Windows Installer necessario per installare la patch ottenuta dalla proprietà [**riepilogo Conteggio parole**](word-count-summary.md) .

-   L'elemento TargetProduct è un elemento contenitore per informazioni su un'applicazione a cui è destinata una patch.

    Se la patch può essere applicata a più applicazioni, possono essere presenti più elementi TargetProduct. Le informazioni contenute nell'elemento TargetProduct vengono estratte dalle trasformazioni incorporate all'interno della patch.

-   L'elemento TargetProductCode contiene il valore della proprietà [**ProductCode**](productcode.md) dell'applicazione di destinazione prima che sia stata applicata la patch.

    Se la patch può essere applicata a più applicazioni, possono essere presenti più elementi TargetProductCode.

-   L'elemento UpdatedProductCode contiene il GUID del codice prodotto dell'applicazione di destinazione dopo l'applicazione della patch.

    Questo elemento è presente solo se la patch modifica il valore della proprietà [**ProductCode**](productcode.md) . Una patch che modifica **ProductCode** viene definita [aggiornamento principale](major-upgrades.md).

-   L'elemento TargetVersion contiene la proprietà [**ProductVersion**](productversion.md) dell'applicazione di destinazione prima dell'applicazione della patch.
-   L'elemento UpdateVersion contiene il valore della proprietà [**ProductVersion**](productversion.md) dell'applicazione di destinazione dopo l'applicazione della patch.

    Questo elemento è presente solo se la patch modifica il valore della proprietà [**ProductVersion**](productversion.md) . Il BLOB XML per una patch che implementa un [piccolo aggiornamento](small-updates.md), noto anche come QFE, non includerà questo elemento. Il BLOB XML per una patch che implementa un aggiornamento secondario, noto anche come Service Pack, includerà questo elemento.

-   L'elemento TargetLanguage contiene il valore della proprietà [**ProductLanguage**](productlanguage.md) dell'applicazione di destinazione prima che sia stata applicata la patch.
-   L'elemento UpdatedLanguages contiene il valore della proprietà [**ProductLanguage**](productlanguage.md) dopo l'applicazione della patch.
-   L'elemento UpgradeCode contiene il valore della proprietà [**UpgradeCode**](upgradecode.md) dell'applicazione di destinazione.
-   L'elemento ObsoletedPatch contiene i codici patch (GUID) delle patch specificate come obsolete da questa patch.

    L'elenco delle patch obsolete viene ottenuto dal [**Riepilogo dei numeri di revisione**](revision-number-summary.md) nel flusso di informazioni di [Riepilogo](summary-information-stream.md) della patch.

-   L'elemento SequenceData contiene informazioni di sequenziazione delle patch per la patch.

    Nel BLOB XML possono essere presenti più elementi SequenceData. Ogni elemento SequenceData contiene le informazioni contenute in una riga della [tabella MsiPatchSequence](msipatchsequence-table.md) della patch. L'elemento SequenceData contiene un sottoelemento ProductCode, Sequence e Attributes per le informazioni nei campi corrispondenti della tabella MsiPatchSequence. Per una descrizione di ogni campo, vedere la sezione relativa alla [tabella MsiPatchSequence](msipatchsequence-table.md) .

## <a name="extracting-applicability-information"></a>Estrazione delle informazioni sull'applicabilità

Nell'esempio seguente viene illustrato come estrarre le informazioni sull'applicabilità per una patch di Windows Installer (file con estensione msp) utilizzando [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa). Il BLOB XML estratto è basato sulla definizione dello schema in MSIPatchApplicability. xsd e viene restituito a szXMLData.


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



Nell'esempio seguente viene illustrato come estrarre le informazioni sull'applicabilità per un Windows Installer patch (file con estensione msp) in formato XML. Il BLOB XML estratto è basato sulla definizione dello schema in MSIPatchApplicability. xsd e restituito in strPatchXML.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Definizione dello schema di applicabilità patch

Copiare il testo seguente nel blocco note o in un altro editor di testo per creare il file di definizione dello schema per le informazioni sull'applicabilità della patch nel BLOB XML. Assegnare al file il nome MSIPatchApplicability. XSD.

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ExtractPatchXMLData**](installer-extractpatchxmldata.md)
</dt> <dt>

[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



