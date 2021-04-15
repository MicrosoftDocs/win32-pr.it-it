---
title: Schema e algoritmi del profilo del modello del dispositivo a colori WCS
description: In questo argomento vengono fornite informazioni sullo schema del profilo del modello di dispositivo con colori WCS e sugli algoritmi associati. Questo argomento contiene le sezioni seguenti OverviewColor Device Model Profile ArchitectureThe CDMP SchemaWCS CDMP v 2.0 Calibration AdditionThe CDMP schema ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTy peMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe CDMP Baseline AlgorithmsCRT modello dispositivo BaselineLCD modello di dispositivo BaselineRGB stampante modello BaselineRGB modello di dispositivo virtuale BaselineCMYK stampante modello BaselineRGB proiettore dispositivo modello BaselineICC modello di dispositivo BaselineRelated argomenti
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Windows Color System (WCS), color Device Model Profile (CDMP)
- WCS (sistema Windows Color), color Device Model Profile (CDMP)
- Gestione colori immagine, profilo modello del dispositivo a colori (CDMP)
- gestione dei colori, profilo del modello del dispositivo a colori (CDMP)
- colori, profilo modello del dispositivo a colori (CDMP)
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- schemi, color Device Model Profile (CDMP)
- algoritmi, color Device Model Profile (CDMP)
- profilo del modello del dispositivo a colori (CDMP)
- CDMP (Color Device Model Profile)
- Profilo modello dispositivo a colori WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b671bf97625b00c99060e65be4d39c44e5b35f
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554325"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>Schema e algoritmi del profilo del modello del dispositivo a colori WCS

In questo argomento vengono fornite informazioni sullo schema del profilo del modello di dispositivo con colori WCS e sugli algoritmi associati.

In questo argomento sono incluse le sezioni seguenti:

-   [Overview](#overview)
-   [Architettura del profilo del modello del dispositivo a colori](#color-device-model-profile-architecture)
-   [Schema CDMP](#the-cdmp-schema)
-   [Aggiunta calibrazione CDMP v 2.0 WCS](#wcs-cdmp-v20-calibration-addition)
-   [Elementi dello schema CDMP](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [NamespaceVersion](#namespaceversion)
    -   [Versione](#namespaceversion)
    -   [Documentazione](#documentation)
    -   [Elemento CRTDevice](#crtdevice-element)
    -   [Elemento LCDDevice](#lcddevice-element)
    -   [Elemento ProjectorDevice](#projectordevice-element)
    -   [Elemento ScannerDevice](#scannerdevice-element)
    -   [Elemento CameraDevice](#cameradevice-element)
    -   [Elemento RGBPrinterDevice](#rgbprinterdevice-element)
    -   [Elemento CMYKPrinterDevice](#cmykprinterdevice-element)
    -   [Elemento RGBVirtualDevice](#rgbvirtualdevice-element)
    -   [PlugInDeviceType](#plugindevicetype)
    -   [RGBVirtualMeasurementType](#rgbvirtualmeasurementtype)
    -   [GammaType](#gammatype)
    -   [GammaOffsetGainType](#gammaoffsetgaintype)
    -   [GammaOffsetGainLinearGainType](#gammaoffsetgainlineargaintype)
    -   [ToneResponseCurvesType](#toneresponsecurvestype)
    -   [GamutBoundarySamplesType](#gamutboundarysamplestype)
    -   [FloatPairList](#floatpairlist)
    -   [CMYKPrinterMeasurementType](#cmykprintermeasurementtype)
    -   [RGBPrinterMeasurementType](#rgbprintermeasurementtype)
    -   [RGBCaptureMeasurementType](#rgbcapturemeasurementtype)
    -   [OneBasedIndex](#onebasedindex)
    -   [RGBProjectorMeasurementType](#rgbprojectormeasurementtype)
    -   [DisplayMeasurementType](#displaymeasurementtype)
    -   [MeasurementConditionsType](#measurementconditionstype)
    -   [GeometryType](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeCMYKSampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeCMYKType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [Algoritmi di base di CDMP](#the-cdmp-baseline-algorithms)
    -   [Baseline modello di dispositivo CRT](#crt-device-model-baseline)
    -   [Linea di base del modello di dispositivo LCD](#lcd-device-model-baseline)
    -   [Baseline modello dispositivo stampante RGB](#rgb-printer-device-model-baseline)
    -   [Linea di base del modello di dispositivo virtuale RGB](#rgb-virtual-device-model-baseline)
    -   [Baseline modello di dispositivo stampante CMYK](#cmyk-printer-device-model-baseline)
    -   [Baseline modello di dispositivo proiettore RGB](#rgb-projector-device-model-baseline)
    -   [Baseline del modello di dispositivo ICC](#icc-device-model-baseline)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Questo schema viene utilizzato per specificare il contenuto di un profilo del modello del dispositivo a colori (CDMP). Gli algoritmi di base associati sono descritti di seguito.

Lo schema DMP (Basic Device Model Profile) è costituito dai dati di misurazione del campionamento.

Il componente di campionamento del XML Schema DMP fornisce supporto per gli obiettivi di misurazione dei colori di base, concentrandosi su destinazioni e destinazioni standard più comuni ottimizzate per i modelli di dispositivo di base.

Il profilo del dispositivo fornisce inoltre informazioni specifiche sul modello di dispositivo di destinazione e fornisce un criterio che il modello di dispositivo di fallback di base può utilizzare se il modello di destinazione non è disponibile. Le istanze del profilo possono includere estensioni private mediante meccanismi di estensione XML standard.

## <a name="color-device-model-profile-architecture"></a>Architettura del profilo del modello del dispositivo a colori

![Diagramma che mostra le informazioni che costituiscono un profilo del modello di dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>Schema CDMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
        <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
        <xs:element name="WhitePointName">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="D50"/>
              <xs:enumeration value="D65"/>
              <xs:enumeration value="A"/>
              <xs:enumeration value="F2"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:choice>
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a>Aggiunta calibrazione CDMP v 2.0 WCS

L'elemento **ColorDeviceModel** dello schema CDMP è stato aggiornato in Windows 7 in modo da includere il nuovo elemento Calibration. Di seguito viene illustrata la modifica allo schema CDMP.


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a>Elementi dello schema CDMP

> [!Note]  
> Le primarie sono esempi primari di rosso, verde, blu, nero e bianco. Una rampa primaria è una rampa tonale da minima luminanza a un valore primario completo. Il numero massimo di voci in una rampa di tono è 4096.

 

> [!Note]  
> Per i dati di misurazione è necessario DMPs.

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

Questo elemento è di tipo ColorDeviceModel.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="colordevicemodel"></a>ColorDeviceModel

Questo elemento è una sequenza dei sottoelementi seguenti

1.  Stringa ProfileName,
2.  stringa di descrizione facoltativa,
3.  stringa autore facoltativa,
4.  facoltativo MeasurementConditions MeasurementConditionsType,
5.  Self-Luminous valore booleano,
6.  MaxColorant float,
7.  MinColorant float,
8.  Scelta di elementi
    1.  CRTDevice,
    2.  LCDDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. Estensione facoltativa ExtensionType

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo. Gli elementi secondari stringa hanno un massimo di 10.000 caratteri. Il sottoelemento MaxColorant deve essere maggiore o uguale a zero (0) e maggiore del sottoelemento MinColorant. Il valore di MinColorant può essere negativo.

### <a name="namespaceversion"></a>NamespaceVersion

xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Versione

Version = "1,0" con Windows Vista.

**Condizioni di convalida:** Qualsiasi valore di versione &gt; 0,1 o &lt; = 2,0 è valido per supportare le modifiche non di rilievo nel formato.

### <a name="documentation"></a>Documentazione

Schema del profilo del modello di dispositivo.

Copyright (C) Microsoft. Tutti i diritti sono riservati.

### <a name="crtdevice-element"></a>Elemento CRTDevice

Questo elemento è una sequenza di sottoelementi di un DisplayMeasurementType MeasurementData.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="lcddevice-element"></a>Elemento LCDDevice

Questo elemento è una sequenza di sottoelementi di un DisplayMeasurementType MeasurementData.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="projectordevice-element"></a>Elemento ProjectorDevice

Questo elemento è una sequenza di sottoelementi di un RGBProjectorMeasurementType MeasurementData.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="scannerdevice-element"></a>Elemento ScannerDevice

Questo elemento è una sequenza di sottoelementi di un RGBCaptureMeasurementType MeasurementData

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="cameradevice-element"></a>Elemento CameraDevice

Questo elemento è una sequenza di sottoelementi di un RGBCaptureMeasurementType MeasurementData

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="rgbprinterdevice-element"></a>Elemento RGBPrinterDevice

Questo elemento è una sequenza di sottoelementi di un RGBPrinterMeasurementType MeasurementData.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="cmykprinterdevice-element"></a>Elemento CMYKPrinterDevice

Questo elemento è una sequenza di sottoelementi di un CMYKPrinterMeasurementType MeasurementData.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="rgbvirtualdevice-element"></a>Elemento RGBVirtualDevice

Questo elemento è una sequenza di sottoelementi di un RGBVirtualMeasurementDataType.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="plugindevicetype"></a>PlugInDeviceType

Questo elemento è una sequenza di un GUID GUIDType e di tutti gli elementi secondari.

**Condizioni di convalida:** Il GUID viene usato per trovare la corrispondenza con il GUID della dll del plug-in DM. Sono presenti un massimo di 100.000 sottoelementi personalizzati.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Questo elemento è una sequenza composta da

1.  Gruppo RGBPrimariesGroup
2.  Scelta di
3.  -   Gamma
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   Elementi ToneResponseCurves

4.  GamutBoundarySamplesType GamutBoundarySamples facoltativo
5.  DateTime TimeStamp

**Condizioni di convalida:** Ogni sottoelemento di questi tipi presenta le proprie condizioni di convalida.

### <a name="gammatype"></a>GammaType

Questo elemento è un tipo complesso costituito dall'attributo

-   NonNegativeFloatType gamma

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Questo elemento è un tipo complesso costituito dagli attributi

-   NonNegativeFloatType gamma
-   Offset NonNegativeFloatType
-   Ottieni NonNegativeFloatType

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Questo elemento è un tipo complesso costituito dagli attributi

-   NonNegativeFloatType gamma
-   Offset NonNegativeFloatType
-   Ottieni NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Questo elemento è una sequenza di

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

L'elemento dispone anche di un attributo TRCLength di tipo unsignedInt.

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Questo elemento è una sequenza di RGBTypes RGB.

**Condizioni di convalida:** Numero massimo di occorrenze attualmente non vincolate, da raggiungere in base ai commenti del settore.

### <a name="floatpairlist"></a>FloatPairList

Questo elemento è un tipo semplice di elenco di coppie di float.

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

Questo elemento è un

1. sequenza dell'elemento cubocolori costituito da una sequenza di NonNegativeCMYKSampleType di esempio

2. TimeStamp dateTime (attributo).

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Questo elemento è un

1. sequenza dell'elemento cubocolori costituito da una sequenza di NonNegativeRGBSampleType di esempio

2. TimeStamp dateTime (attributo).

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Questo elemento è una sequenza di

1.  ComplexType PrimaryIndex
2.  1.  OneBasedIndex bianco
    2.  OneBasedIndex nero facoltativo
    3.  OneBasedIndex rosso facoltativo
    4.  OneBasedIndex verde facoltativo
    5.  OneBasedIndex blu facoltativo
    6.  OneBasedIndex ciano facoltativo
    7.  OneBasedIndex magenta facoltativo
    8.  OneBasedIndex giallo facoltativo

3.  NeutralIndices delle righe di OneBasedIndex
4.  Sequenza ColorSamples di NonNegativeRGBSampleType di esempio

L'elemento include anche un attributo TimeStamp dateTime.

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="onebasedindex"></a>OneBasedIndex

Questo elemento è un tipo semplice di base di limitazione senza segno int con valore minInclusive = "1".

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Questo elemento è una sequenza di

1.  Gruppo RGBPrimariesGroup
2.  elemento ColorSamples costituito dalla sequenza di NonNegativeRGBSampleType di esempio

L'elemento include anche un attributo TimeStamp dateTime.

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Questo elemento è una sequenza di

1.  RGBPrimariesGroup gruppo
2.  GrayRamp della sequenza di NonNegativeRGBType di esempio
3.  RedRamp della sequenza di NonNegativeRGBType di esempio
4.  GreenRamp della sequenza di NonNegativeRGBType di esempio
5.  BlueRamp della sequenza di NonNegativeRGBType di esempio

L'elemento DisplayMeasurementType include anche un attributo TimeStamp dateTime.

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

MeasurementConditionsType è una sequenza di sottoelementi che contiene:

1.  Valore di enumerazione di stringhe con limitazione dello spazio dei colore di "CIE XYZ"
2.  scelta facoltativa dell'enumerazione WhitePoint NonNegativeXYZType o WhitePointName String dei valori D50, D65, A o F2
3.  Geometria GeometryType
4.  ApertureSize Integer in millimetri

Le impostazioni predefinite sono:

1.  Stampanti RGB e CMYK:
    1.  MeasurementSpaceType CIE XYZ
    2.  WhitePointValue D50
    3.  0/45 GeometryType
    4.  ApertureSize 10mm
2.  Scanner
    1.  MeasurementSpaceType CIE XYZ
    2.  WhitePointValue D50
    3.  0/45 GeometryType
    4.  ApertureSize 10mm
3.  Visualizza e dispositivo virtuale RGB:
    1.  MeasurementSpaceType CIE XYZ
    2.  WhitePointValue D65
    3.  0/45 GeometryType
    4.  ApertureSize 10mm
4.  Fotocamere
    1.  MeasurementSpaceType CIE XYZ
    2.  WhitePointValue D65
    3.  GeometryType diretto
    4.  ApertureSize 10mm

**Condizioni di convalida:** La convalida di ogni sottoelemento è determinata dalle condizioni di convalida per tali sottoelementi. Se manca un sottoelemento, viene usato il tipo di modello di dispositivo predefinito specifico.

### <a name="geometrytype"></a>GeometryType

string

Valori di enumerazione:

-   "0/45"
-   "0/diffuso"
-   "diffuso/0"
-   Diretto

**Condizioni di convalida:** Qualsiasi valore, ad eccezione dei valori enumberation elencati, non è valido. Queste informazioni non modificheranno il comportamento di elaborazione della linea di base.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Questo elemento è una sequenza di

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="nonnegativecmyksampletype"></a>NonNegativeCMYKSampleType

Questo elemento è una sequenza di

1.  NonNegativeCMYKType CMYK
2.  NonNegativeXYZType CIE XYZ

L'elemento include anche una stringa di Tag Attribute facoltativa

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Questo elemento è una sequenza di

1.  NonNegativeRGBType RGB
2.  NonNegativeXYZType CIE XYZ

L'elemento include anche una stringa di Tag Attribute facoltativa

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="nonnegativecmyktype"></a>NonNegativeCMYKType

Questo elemento è costituito da attributi

1.  C float
2.  Float M
3.  Float Y
4.  K float

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Questo elemento è costituito da attributi

1.  Float R
2.  G float
3.  Float B

**Condizioni di convalida:** Per essere determinato dal feedback del settore.

### <a name="extensiontype"></a>ExtensionType

L'elemento ExtensionType è una sequenza di qualsiasi tipo di sottoelemento e viene usato per informazioni proprietarie da applicazioni non Microsoft.

**Condizioni di convalida:** Questo elemento è facoltativo. Possono essere presenti al massimo 1000 sottoelementi di estensione.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

L'elemento NonNegativeXYZType è costituito da NonNegativeFloatType tre elementi a virgola mobile IEEE a precisione singola denominati "X", "Y" e "Z". Questi valori sono limitati ai valori di misurazione dei profili DMP. Queste misurazioni possono essere di tipo assoluto (non relativo) CIE XYZ 1931 o assoluti (non relativi) CIE XYZ 1931 Direct (transmissal) in candele per metro unità quadrate.

**Condizioni di convalida:** Solo i valori reali sono validi e i valori di misurazione CIE XYZ negativi non sono validi. Poiché si tratta di valori assoluti, i valori possono essere maggiori di 1,0 f. Limite ragionevole per qualsiasi "X", "Y" o "Z". il valore è arbitrariamente impostato su 10000.0 f.

### <a name="xyztype"></a>XYZType

L'elemento XYZType è costituito da tre valori a virgola mobile IEEE con precisione singola: "X", "Y" e "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Algoritmi di base di CDMP

### <a name="crt-device-model-baseline"></a>Baseline modello di dispositivo CRT

Per comprendere questo modello, è necessario considerare sia il processo di caratterizzazione che la modellazione del dispositivo. Nel processo di caratterizzazione, le misurazioni XYZ vengono eseguite prima sui colori ottenuti riempiendo il buffer di visualizzazione di un dispositivo di visualizzazione CRT. I valori di esempio seguenti genereranno dati validi per il modello di dispositivo CRT Baseline:

Rosso: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blu: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrals: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

È inoltre possibile utilizzare incrementi diversi da 15 e incrementi non lineari. Ogni rampa rossa, verde, blu e neutra deve contenere almeno tre campioni, ma è consigliabile fornire più esempi. È necessario fornire esempi per i puri rossi, verdi, blu, neri e bianchi. Gli esempi non devono essere distanziati in modo uniforme.

Il processo di creazione della matrice tristimolo è costituito da due passaggi. Per prima cosa, stimare il valore XYZ del punto nero o il bagliore. Questo passaggio si basa in larga misura sul lavoro di Bernas \[ 3 \] con una funzione oggettiva leggermente modificata per l'ottimizzazione non lineare. In secondo luogo, calcolare la matrice tristimolo in base al risultato del passaggio uno e anche da un calcolo della media di tutte le misurazioni per canale, non solo da quello per il numero massimo di numeri digitali.

Ognuno di questi passaggi contiene procedure dettagliate. Il punto di partenza è costituito dalle rampe (17 passaggi nell'esempio) per ogni canale R, G e B. Quando le misurazioni XYZ sono tracciate sul piano *XY* di cromaticità, una situazione tipica è illustrata nella figura 1. Il primo passaggio consiste nella risoluzione di un problema di ottimizzazione non lineare per individuare il punto nero "migliore adattamento" che ridurrà al minimo la tendenza nella cromaticità come uno attraversa lungo i canali R, G e B. In base a Bernas \[ 3, cerchiamo \] ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ) che riduce al minimo la funzione Objective seguente:

![Mostra la funzione objective in cui SR, SG e SB sono il set di punti dati nei canali R, G e B.](images/cdmp-formula1.png)

dove *s <sub>R</sub>*,*s <sub>G</sub>* e *s <sub>B</sub>* sono il set di punti dati corrispondente ai punti sui canali R, G e b. Per qualsiasi set *S*, definire:

![Mostra una formula per la definizione di tutti i set.](images/cdmp-formula2.png)

Nell'esempio precedente, \| *s* \| è la cardinalità di *s*, ovvero il numero di punti nel set *S*. ![ Mostra una formula per la cromaticità di un punto.](images/cdmp-formula3.png) Coordinate di cromaticità del punto che ![ Mostra un formaula per un punto.](images/cdmp-formula4.png) , quindi, ![ Mostra una formula per la media o il centro della massa. ](images/cdmp-formula5.png) , è la media, o il centro della massa, di tutti i punti nel set *S* nel piano di cromaticità. Quindi, ![ Mostra una formula per la somma di un secondo istanti di punti.](images/cdmp-formula6.png) è la somma di secondi di punti relativi al centro della massa ed è una misura della diffusione dei punti. Infine, ![ Mostra una formula per la misura totale della distribuzione di tre cluster di punti.](images/cdmp-formula7.png) è una misura totale di come la distribuzione dei tre cluster di punti riguarda i rispettivi centri di massa.

Nel calcolo di ![ viene mostrata una formula di f (X, Y, Z; XK,, di ZK, ZK).](images/cdmp-formula8.png) , se ![ Mostra una formula per X. ](images/cdmp-formula9.png) , il calcolo viene ignorato e la cardinalità di *S* viene modificata di conseguenza.

Nonostante la complessità apparente della funzione oggettiva, è una somma dei quadrati di molte funzioni differenziabili in *X <sub>k</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 punti 2 *XY* -Components 3 Channels = 102, nell'esempio) e, pertanto, è suscettibile alle tecniche standard non lineari minime, ad esempio l'algoritmo Levenberg-Marquardt, che è l'algoritmo usato in WCS. Si noti che la funzione dell'obiettivo precedente è diversa da quella suggerita in Bernas \[ 3 \] in quanto quest'ultima misura la varianza delle distanze dal centro della massa, in modo che la varianza sia zero quando i punti sono equidistanti dal centro della massa, anche se possono diffondersi. Nell'esempio, la dispersione dei punti è contollata direttamente usando i secondi istanti.

Come per qualsiasi algoritmo iterativo per il problema dei minimi quadrati non lineari, Levenberg-Marquardt richiede una supposizione iniziale. Esistono due candidati evidenti. Uno è (0, 0, 0); l'altro è il punto nero misurato. Per la CTE, il punto nero misurato viene usato per la prima volta come supposizione iniziale. Se viene superato un massimo di 100 iterazioni senza raggiungere una soglia di una distanza media di 0,001 di ogni punto dal centro di massa (che corrisponde a un valore soglia di (0,001) 17 3 = 0,000051 per la funzione Objective), viene eseguito un altro ciclo di iterazioni con l'ipotesi iniziale di (0, 0, 0). La stima risultante del punto nero è XYZ rispetto alla stima migliore del ciclo di iterazione precedente (con il punto nero misurato come supposizione iniziale). Utilizzare la stima che fornisce il valore più piccolo per la funzione Objective. La scelta di iterazioni 100 e la distanza degli errori di 0,001 sono state selezionate empiricamente. Nelle versioni future, potrebbe essere ragionevole parametrizzare la distanza degli errori.

Il risultato del passaggio uno è il punto nero stimato ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ). Il secondo passaggio consiste nel determinare la matrice tristimolo calcolando la media della cromaticità dei punti nei tre cluster ottenuti nel passaggio 1. Per CRT, questa operazione viene eseguita principalmente per ridurre al minimo gli effetti degli errori di misurazione. I punti usati per la media della cromaticità devono essere gli stessi punti usati nell'ottimizzazione nel passaggio uno. In altre parole, se il primo punto (Digital count 15, nell'esempio) in ogni rampa viene eliminato nel passaggio di ottimizzazione, lo stesso deve essere eseguito nella media. Se ![ Mostra le formule della cromaticità media per le coordinate nei canali rosso e verde.](images/cdmp-formula10.png) e ![ Mostra una formula della cromaticità media per le coordinate nel canale blu.](images/cdmp-formula11.png) sono le coordinate della cromaticità media dei canali rosso, verde e blu, quindi la procedura seguente determina la matrice tristimolo. Per prima cosa, risolvere il 3? 3 sistema lineare:

![Mostra la prima parte della procedura per risolvere un sistema lineare 3? 3.](images/cdmp-formula12.png)

![Mostra la seconda parte del sistema lineare 3? 3.](images/cdmp-formula13.gif)![Mostra il valore di t pedice b alla fine della seconda parte del sistema lineare 3? 3.](images/cdmp-formula14.gif)

*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>w</sub>*

![Mostra la parte finale della procedura per risolvere un sistema lineare 3? 3.](images/cdmp-formula15.png)

Dopo che la matrice tristimolo è stata determinata, la determinazione delle curve di tono segue l'approccio standard. Per le visualizzazioni CRT, si presuppone che i singoli canali seguano il modello "GOG":

![Mostra la formula per il modello ' G O G '.](images/cdmp-formula16.png)

dove *k <sub>g</sub>* è il "guadagno", 1-*k <sub>g</sub>* è "offset" e? è il "gamma". La matrice inversa della matrice tristimolo viene applicata ai dati XYZ degli neutri per ottenere i dati RGB lineari, che vengono quindi correlati con i valori RGB digitali usando la regressione non lineare sul modello GOG. Queste caratteristiche non devono essere uguali per i canali R, G e B e in genere non sono uguali.

Berns \[ 1 \] : Berns, *Billmeyer e spugnos, principi della tecnologia dei colori*, 3 <sub>Rd</sub> ed. John Wiley & Sons (2000).

Berns \[ 2 \] : Berns e Katoh, la funzione di trasferimento da digitale a radiometrica per i monitor CRT controllati da computer, il *Simposio esperto cie di 97 colori standard per la tecnologia di imaging*, nov. 1997.

Berns \[ 3 \] : Bernas, Fernandez e Taplin, stima Black-Level le emissioni di Computer-Controlled Visualizzazioni, *ricerca a colori e applicazione*, 28:379-383 dei periodici Wiley, Inc. (2003)

Kang \[ 1 \] : Kang, *tecnologia dei colori per dispositivi di imaging elettronico*, spie (1997)

Katoh \[ 1 \] : Katoh, Deguchi e Berns, una descrizione accurata della proposta di monitoraggio CRT (II) per un'estensione del metodo CIE e la relativa verifica, *opt. Rev.* 8:397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Linea di base del modello di dispositivo LCD

La linea di base del modello di dispositivo LCD è simile alla baseline del modello di dispositivo CRT. In questa sezione vengono illustrati i modi in cui la modellazione LCD è diversa dalla modellazione CRT.

Una differenza consiste nel fatto che non è possibile presupporre che gli schermi LCD seguano il modello GOG usato per CRT e che le curve di tono siano ottenute dall'interpolazione dei dati misurati. Per questo motivo, è consigliabile campionare l'asse neutro del dispositivo con maggiore frequenza.

Di seguito sono riportati alcuni valori di esempio tipici che possono generare dati validi per la baseline del modello di dispositivo LCD:

Rosso: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blu: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

Il processo di media delle cromie di colore misurato per ottenere la cromaticità per le primarie del dispositivo è più importante per gli LCD rispetto a CRT. Quando le misurazioni XYZ sono tracciate sulla superficie *XY* , una situazione tipica è illustrata nella figura 1. Si noti come la cromaticità si allontana verso il punto nero. Questo perché tutti gli LCD hanno una certa quantità di perdite di luce.

![Diagramma che mostra un grafico della cromaticità utilizzando dati non elaborati senza correzione.](images/cdmp-lcd-dmp-figure1.png)

**Figura 1** : diagramma di cromaticità con dati non elaborati senza correzione

Quando viene sottratto dalle misurazioni XYZ non elaborate, una situazione tipica è illustrata nella figura 2. I punti di TImpossibile sono ora raggruppati in tre centri, sebbene non rientrino in modo identico. Il processo di mediazione descritto per CRT migliora notevolmente i risultati per i monitor LCD.

![Diagramma che mostra un grafico della cromaticità utilizzando dati non elaborati con un punto nero modificato.](images/cdmp-lcd-dmp-figure2.png)

**Figura 2** : diagramma di cromaticità con i dati con punto nero modificato

### <a name="rgb-capture-device-model-baseline"></a>Linea di base modello di acquisizione RGB

Il modello di dispositivo di acquisizione RGB di base è una sottoclasse della classe IDeviceModel. Nella caratterizzazione colorimetrico dei dispositivi di acquisizione dei colori, ad esempio scanner e fotocamere digitali, viene usato l'approccio seguente. Una destinazione costituita da patch di colore con valori CIE XYZ noti viene acquisita usando il dispositivo di acquisizione. Il risultato dell'acquisizione è un'immagine bitmap RGB in cui il colore di ogni patch è codificato in un valore RGB. Questi valori RGB del dispositivo sono specifici di un dispositivo di acquisizione specifico. L'obiettivo della caratterizzazione colorimetrico è stabilire una relazione empirica tra i valori RGB del dispositivo e i valori CIE XYZ o una trasformazione matematica da RGB a XYZ che modella il più accuratamente possibile il comportamento del dispositivo di acquisizione.

Una trasformazione matematica di questo tipo può essere modellata ragionevolmente da polinomi di basso livello. Questa procedura è descritta in dettaglio in letteratura, ad esempio Kang \[ 92 \] , Kang \[ 97 \] . In Kang \[ 97 \] viene segnalato un approccio che usa un set di tre polinomi con 3, 6, 8, 9, 11, 14 o 20 termini nelle variabili R, G e B, mentre i tre polinomi regressione rispettivamente nei componenti X, Y, Z dello spazio CIE XYZ. Per il polinomio a 20 termini, il formato è:

![Mostra il polinomio a 20 termini.](images/cdmp-formula20.png)

Sono presenti espressioni simili per Y e Z. La tecnica matematica per l'adattamento dei polinomi rientra in "regressione lineare multivariata" ed è descritta in qualsiasi testo elementare in Statistics.

Questo metodo di regressione lineare soffre di non ridurre al minimo la funzione dell'obiettivo "Right". Per impostazione predefinita, la regressione lineare trova la soluzione dei minimi quadrati, che implica che i coefficienti ottenuti ridurranno al minimo la somma totale dei quadrati di errori nello spazio sottostante, o in modo equivalente, la somma dei quadrati delle distanze euclidee. In pratica, si vuole ridurre al minimo la somma dei quadrati di? Es, dove? E è uno degli standard accettati, ad esempio CIE94. La riduzione di questa funzione oggettiva è un problema di regressione non lineare.

Nel nuovo motore, Lab per XYZ è lo spazio dei colori CIE in cui viene regressione e viene usato il polinomiale cubico a 20 termini come modello per il dispositivo di acquisizione, o coefficienti ls, come, BS, in modo che i polinomi seguenti riducano al minimo la somma dei quadrati di? E <sub>CIE94</sub> .

![Mostra un set di formule polinomiali.](images/cdmp-formula21.png)

La soluzione ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) nello spazio numerico reale 60 dimensionale **R** 203 deve essere tale che l'errore totale seguente sia ridotto a icona:

![Mostra l'errore totale da ridurre a icona.](images/cdmp-formula22.png)

dove la sommatoria è attraverso tutte le coppie di punti dati (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) nel set di dati campionati più punti di controllo aggiuntivi per essere descritti in dettaglio nell'esempio riportato di seguito. Si tratta di un problema di regressione non lineare perché i parametri *?<sub> i</sub>*, *a <sub>i</sub>*, * <sub>i</sub>* entri nella funzione objective in modo non lineare (non quadratico).

Poiché la funzione Objective? è una funzione non lineare (e non quadratica) dei parametri *?<sub> i</sub>*, *a <sub>i</sub>* e * <sub>i</sub>* è necessario ricorrere a tecniche iterative per risolvere il problema di ottimizzazione. Poiché il form della funzione Objective è una somma di quadrati, viene usata una tecnica di ottimizzazione standard denominata Levenberg-Marquardt algoritmo. Viene considerato il metodo preferito per i problemi non lineari con i minimi quadrati. Per gli algoritmi iterativi come Levenberg-Marquardt, è necessario fornire una supposizione iniziale. Una buona supposizione iniziale è in genere cruciale nell'individuare il valore minimo corretto. In questo caso, un candidato valido per l'ipotesi iniziale è la soluzione del problema di regressione lineare. Per prima cosa, ridurre al minimo la somma del quadrato delle distanze euclidee nello spazio Lab definendo una funzione di obiettivo quadratico:

![Mostra una funzione dell'obiettivo quadratico definita.](images/cdmp-formula23.png)

La soluzione matematica a questo problema "lineare con i minimi quadrati" è nota. Perché *?<sub></sub>viene visualizzato solo nella* modellazione *L* , *a <sub>i</sub>* viene visualizzato solo nella modellazione *u* e * <sub>i</sub>* viene visualizzato solo nella modellazione *v* ; il problema di ottimizzazione può essere scomposto in tre problemi, uno per *L*, uno per *u* e uno per *v*. Prendere in considerazione le equazioni *L* . (Le equazioni *u* e le equazioni *v* seguono esattamente lo stesso argomento). Il problema di ridurre al minimo la somma dei quadrati di errori in *L* può essere dichiarato come la risoluzione dell'equazione di matrice seguente nel senso minimo dei quadrati:

![Mostra un'equazione della matrice per L.](images/cdmp-formula24.png)

dove *N* è il numero totale di punti dati (punti campionati originali più punti di controllo creati in un modo descritto di seguito). In genere, *N* è molto più grande di 20, quindi l'equazione precedente è troppo determinata, richiedendo una soluzione con almeno quadrati. Una soluzione form chiusa per **?** disponibile:

![Mostra una soluzione form chiusa.](images/cdmp-formula25.png)

In pratica, la valutazione diretta tramite la soluzione modulo chiuso non viene utilizzata perché contiene proprietà numeriche scarse. Al contrario, un tipo di algoritmo di factorzzazione della matrice viene applicato alla matrice coefficiente, che riduce il sistema di equazioni a una forma canonica. Nell'implementazione corrente, la scomposizione di valori singolari (SVD) viene applicata alla matrice **R** e quindi il sistema decomposto risultante viene risolto.

La soluzione per il problema di regressione lineare, indicata da, ![ Mostra la soluzione al problema di regressione lineare.](images/cdmp-formula26.png) , viene usato come punto iniziale dell'algoritmo Levenberg-Marquardt. In questo algoritmo viene calcolato un passaggio di valutazione che dovrebbe spostare il punto più vicino alla soluzione ottimale. Il passaggio di valutazione soddisfa un set di equazioni lineari che dipendono dal valore funzionale e dai valori dei derivati nel punto corrente. Per questo motivo, i derivati della funzione Objective? per quanto riguarda i parametri *?<sub> i</sub>*, *i <sub></sub> <sub></sub> sono gli* input obbligatori per l'algoritmo Levenberg-Marquardt. Sebbene esistano 60 parametri, è disponibile un collegamento che consente di calcolare un numero molto inferiore. Dalla regola della catena di calcolo,

![Mostra un'equazione che consente un collegamento usando la regola della catena di calcolo.](images/cdmp-formula27.png)

dove *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub></sub>* i,*v <sub>i</sub>* è il valore CIELAB del punto di campionamento *i* , e *R <sub>IJ</sub>* è la voce *(i*,*j* ) della matrice **r** definita sopra. Quindi, invece di calcolare i derivati per i parametri di 60, è possibile calcolare i derivati per *L*,*a* e *b* usando le differenze di avanzamento numerico.

È anche necessario impostare un criterio di arresto per gli algoritmi iterativi. Nell'implementazione corrente, le iterazioni vengono interrotte se il DECIE94 quadrato medio è minore di 1 oppure il numero di iterazioni eseguite ha superato 10. Il numero 10 deriva dall'esperienza pratica che se le prime iterazioni non riducono significativamente l'errore, altre iterazioni non aiuteranno molto oltre lo scorrimento del punto in modo oscillante, ovvero l'algoritmo potrebbe non essere convergente. Anche nel caso in cui l'algoritmo si differenzia, è possibile verificare che il DECIE94 non sia peggiore rispetto a quello iniziato, ovvero con i parametri ottenuti dalla regressione lineare.

Anche con il metodo precedente di regressione non lineare, esistono diversi problemi con l'adattamento. Un problema consiste nel fatto che i polinomi tendono a superare o sottobattere i punti dati. Le massime e minime locali artificiali possono essere introdotte nel processo di adattamento. Questa operazione può essere neutralizzata usando polinomi di basso livello, motivo per cui non è consigliabile usare più di tre gradi. Un aspetto più grave dell'Overshooting o dell'abbattimento è che, mentre un polinomiale può assumere un valore reale teoricamente, lo spazio che tenta di modellare in genere presenta vincoli fisici e pratici. CIE XYZ deve avere tutti i X, Y, Z non negativi, che è un vincolo fisico. In pratica, accettano solo valori nella grandezza di centinaia, non di migliaia o superiori. Analogamente, CIELAB o CIELUV presenta vincoli fisici e pratici. Quando lo spazio RGB viene riempito sufficientemente con i punti di campionamento, il problema dell'Overshooting o dell'overshooting non è grave. Tuttavia, i punti RGB acquisiti dal dispositivo di acquisizione in genere non riempiono lo spazio RGB in modo uniforme. I punti possono riempirsi solo interno del 80% del cubo RGB, o peggiori, possono trovarsi in un collettore di dimensioni inferiori. Quando si verifica questo problema, i polinomi regressione possono eseguire un processo scadente per estrapolare i valori oltre i punti dati, a volte restituendo stime non realistiche. Si desidera un modello che restituisce sempre valori ragionevolmente realistici. Questa operazione richiede un metodo che possa controllare in modo efficace il comportamento dei limiti dei polinomi di regressione imponendo un costo aggiuntivo per i polinomi che si comportano in modo irregolare vicino al limite del cubo RGB. Un'ulteriore misura per assicurarsi che i polinomi restituiscano sempre i valori realistici vengono applicati ritagliando l'output all'interno del locus spettrale CIE.

È a questo punto che la modellazione dello scanner e la modellazione della fotocamera divergeno tra loro. Si prevede che il modello di fotocamera venga estrapolato nelle aree oltre i punti campionati, incluse le "evidenziazioni speculari", per il modello di scanner non è necessaria la stessa estrapolazione. Si prevede che la destinazione dello scanner copra una caratterizzazione simile al materiale stampato da analizzare. Il modello dello scanner è ancora necessario per essere affidabile, nel senso che non deve restituire valori non realistici, ma non è necessaria un'estrapolazione ben oltre la destinazione di caratterizzazione. Per garantire l'affidabilità, l'L-polinomiale precedente viene ritagliato a 100, ovvero il modello polinomiale è forzato a non estrapolare oltre "dmin" della destinazione dello scanner.

Si prevede che il modello di fotocamera venga estrapolato in evidenza speculari, quindi il ritaglio a 100 è indesiderato. Viene invece utilizzato l'algoritmo seguente.

I punti di controllo artificiali vengono introdotti per controllare il comportamento dei polinomi in aree con campionamento insufficiente. Inserendo in modo strategico questi punti di controllo con i valori appropriati, questi vengono usati per eseguire il pull dei polinomi nella direzione richiesta. Nell'implementazione corrente, vengono usati otto punti di controllo corrispondenti agli angoli del cubo RGB. Se i valori del dispositivo vengono normalizzati in Unity, questi punti sono:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Ad eccezione del bianco *R*  = *G*  = *B* = 1, associato a un valore CIELAB di *L* = 100, *u*  = *v* = 0, viene usato l'algoritmo di estrapolazione seguente per determinare il valore CIELAB appropriato da associare a. In genere, per un determinato (*r*,*g*,*B* ), un peso è associato a ogni (*r <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) nel set di dati campionati. Esistono due obiettivi per assegnare il peso. In primo luogo, il peso è inversamente proporzionale alla distanza tra (*r*,*g*,*b* ) e (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ). In secondo luogo, si desidera eliminare o assegnare il peso 0 a, punti con una tonalità diversa rispetto al punto specificato (*R*,*G*,*B* ). Per prendere in considerazione la tonalità, considerare i punti che si trovano all'interno di un cono il cui vertice si trova in (0, 0, 0), il cui asse coincide con l'Unione di riga (0, 0, 0) a (*R*,*G*,*B* ) e il cui angolo semi-verticale? soddisfa i cos? = 0,9. Vedere la figura 3 per un'illustrazione di questo cono.

![Diagramma che mostra la forma del quartiere.](images/cdmp-lcd-dmp-figure3.png)

**Figura 3** : filtrare i punti di esempio in base all'angolo e alla distanza. La forma del quartiere raffigurato è solo a scopo illustrativo. La forma effettiva dipende dalla distanza utilizzata; si tratta di un quartiere a forma di rombo se si usa la norma 1.

All'interno di questo cono viene eseguito un secondo filtro basato sulla distanza RGB, che usa la norma 1, definita da

![Mostra la formula per il secondo filtro all'interno del cono.](images/cdmp-formula28.png)

Con il cono corrente, la ricerca iniziale è per i punti che si trovano all'interno di una distanza di 0,1 da (*R*,*G*,*B* ). Se non viene trovato alcun punto all'interno di questo raggio, il raggio viene aumentato di 0,1 e la ricerca viene riavviata. Se le reti tonde successive non sono punti, il raggio viene aumentato di 0,1. Questo processo continua fino a quando il raggio supera MaxDist/5, dove MaxDist = 3, nel caso di 1-Norm. Se non viene trovato alcun punto, il cono viene ingrandito diminuendo la cos? per 0,05, ovvero l'aumento dell'angolo? e riavviare l'intero processo con un raggio crescente. Questo processo continua fino a quando non viene trovato un set di punti non vuoto o cos? raggiunge 0, ovvero il cono si è aperto per diventare un piano. A questo punto, la ricerca viene riavviata aumentando il raggio, ad eccezione del fatto che la ricerca continua fino a quando il raggio raggiunge MaxDist. In questo modo si garantisce che nello scenario peggiore verrà trovato un set di punti non vuoto. L'algoritmo viene riepilogato nel diagramma di flusso della figura 4.

![Diagramma che mostra il flusso dell'algoritmo.](images/cdmp-lcd-dmp-figure4.png)

**Figura 4** : diagramma di flusso per determinare il set di punti di esempio usati nell'estrapolazione per un valore RGB di input

Supponendo che il processo precedente restituisca *un set di* punti non vuoto (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ) e corrispondente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), quindi per ogni punto, viene assegnato un peso *w <sub>i</sub>* , fornito da

![Mostra la formula per un peso per ogni punto.](images/cdmp-formula29.png)

Infine, extrapolant è definito da

![Mostra la definizione di extrapolant.](images/cdmp-formula30.png)

Le equazioni precedenti costituiscono un'istanza dei "Metodi ponderati per la distanza inversa", comunemente detti metodi Shepard. Eseguendo ognuno degli otto punti da EQ (6) attraverso l'algoritmo, vengono ottenuti otto punti di controllo, ognuno con i valori *R*,*G*,*B* e *L*,*a*,*b* , che vengono inseriti nel pool con i dati di esempio originali.

Per assicurarsi che il modello produca sempre valori di colore validi e per l'integrità del sistema e la stabilità dell'intera pipeline di elaborazione dei colori, è necessario eseguire un ritaglio finale all'output del modello polinomiale. La gamma di oggetti visivi CIE è descritta dal componente acromatico (*Y* o *L* ) e dal componente cromatico (*XY* o *a'b '*, correlati allo spazio XYZ da una trasformazione proiettiva). Nell'implementazione corrente viene usata la cromaticità *a'b* , in quanto è direttamente correlata allo spazio CIELUV. Per qualsiasi valore *CIELAB* , prima ritagliare *L* su un valore non negativo:

![Mostra il ritaglio di L a un valore non negativo.](images/cdmp-formula31.png)

Per consentire l'estrapolazione per le evidenziazioni speculari, *L* non viene ritagliato a 100, il limite superiore "convenzionale" per *l* nello spazio Lab.

Successivamente, se *L* = 0, *a* e *b* vengono ritagliati in modo che a *= b =* 0. Se *L* ? 0, calcola

![Mostra la formula se L = 0.](images/cdmp-formula32.png)

Questi sono i componenti di un vettore nel diagramma *a'b* dal punto bianco (*u?'*,*v?'* ) per il colore in questione. Definire il locus spettrale CIE come struttura convessa di tutti i punti (*a'*,*b '* ) con parametri per la lunghezza?:

![Mostra la formula per la lunghezza.](images/cdmp-formula33.png)

dove ![ Mostra le funzioni per la corrispondenza dei colori CIE.](images/cdmp-formula34.png) sono le funzioni di corrispondenza dei colori CIE per l'osservatore di 2 gradi. Se il vettore si trova al di fuori del locus CIE, il colore viene ritagliato fino al punto nel locus CIE che rappresenta l'intersezione tra il locus e la riga definita dal vettore. Vedere Figura 5. Se si è verificato il ritaglio, il valore *a* e *b* viene ricostruito prima sottraendo *un?'* e *b? "* dal troncato *a "* e *b"*, quindi moltiplicando per 13 *L*.

![Diagramma che mostra il grafico per l'algoritmo di ritaglio.](images/cdmp-lcd-dmp-figure5.png)

**Figura 5** : algoritmo di ritaglio per i valori Lab esterni al gamut visivo Cie

Nell'implementazione corrente, il locus spettrale CIE nel piano *a'b* è rappresentato da una curva lineare a tratti con segmenti 35 (corrispondenti a una lunghezza compresa tra 360 e 700 nm). Ordinando i segmenti di linea in modo che i rispettivi angoli in base al punto bianco siano in ordine crescente, che equivale a lunghezze d'onda decrescenti, il segmento di linea che si interseca con il raggio formato dal vettore sopra riportato può essere trovato da una semplice ricerca binaria.

### <a name="rgb-printer-device-model-baseline"></a>Baseline modello dispositivo stampante RGB

Una descrizione del dispositivo di una stampante RGB è costituita dalla creazione di un modello empirico del dispositivo che prevede il colore CIELUV indipendente dal dispositivo per qualsiasi valore RGB specificato

Esistono due modi per costruire il modello empirico. Un modo consiste nell'usare i dati del dispositivo per una stampante RGB e l'altro per usare i dati dei parametri analitici. Nel primo, i dati di misurazione forniti da un utente per un dispositivo di stampa RGB vengono usati per creare la tabella di ricerca 3D (LUT). I dati di misurazione sono costituiti da valori XYZ per le patch RGB campionate in modo uniforme. Le dimensioni di campionamento tipiche sono 9 o 17 per ogni componente. Ogni patch viene misurata con un colorimetro o uno spettrofotometro nello spazio CIE XYZ. Il valore XYZ per una patch viene quindi convertito in valore CIELUV, formando un LUT 3D. Nel modello di dispositivo, il metodo di interpolazione tetraedrica di Sakamoto viene applicato al LUT 3D per stimare i dati CIELUV per i dati RGB specificati. (Conferisce il brevetto US 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[ 1 \] . I due brevetti citati sono scaduti. I dati dei parametri analitici passati nel secondo metodo sono semplicemente un LUT compilato in precedenza. In genere, LUT è stato creato usando il primo metodo, sebbene possa essere creato manualmente.

Nella gestione dei colori corrente la mappa di origine è definita come mappa che passa dallo spazio RGB a uno spazio di colore CIE XYZ indipendente dal dispositivo. La mappa di destinazione viene definita come mappa che passa dallo spazio di colore CIE XYZ indipendente dal dispositivo allo spazio RGB. Si tratta dell'inverso della mappa di origine.

Il modello empirico viene usato direttamente nella mappa di origine. Esegue prima il mapping di un dato RGB dati in un CIELUV dati, che viene convertito in dati XYZ. Nella mappa di destinazione i dati CIE XYZ indipendenti dal dispositivo vengono prima convertiti in dati di CIELUV. Quindi, il modello empirico e il metodo di Newton-Raphson classico vengono usati per stimare i dati RGB migliori per i dati CIELUV. I dettagli sulla conversione da CieLUV a dati RGB sono i seguenti:

Dopo la generazione di un LUT 3D da RGB a CieLUV, la mappa da RGB a LUV viene compilata usando l'interpolazione tetraedrica su RGB. Questa mappa è indicata dalle equazioni seguenti:

![Mostra le equazioni per la mappa da R G B a L U V.](images/cdmp-image125.png)

L'inversione della mappa è costituita dalla risoluzione, per qualsiasi colore ![Mostra L U V.](images/cdmp-image127.png) , il sistema seguente di equazioni non lineari:

![Mostra le equazioni non lineari per lolving qualsiasi colore L U V.](images/cdmp-image129.png)

Nella nuova CTE viene utilizzata un'equazione non lineare basata sul metodo di Newton-Raphson classico. Una supposizione iniziale, o *una precedente* , <sub>prima</sub> di, (R 0, G 0, B 0) viene ottenuta tramite la ricerca di una "matrice di inizializzazione" costituita da una griglia 8x8x8 uniforme di coppie pre-calcolate (RGB, Luv). Viene scelto il Luv corrispondente di RGB più vicino a L \* u \* v \* . Ogni punto della matrice di inizializzazione corrisponde al centro di una cella in modo che le iterazioni non inizino con un punto sulla faccia limite del cubo RGB. In altre parole, l'RGB dei semi viene definito da: STEP = 1/8 s <sub>IJK</sub> = (Step/2 + (i-1) Step, Step/2 + (j-1) STEP, Step/2 + (k-1) Step) with i, j, k = 1... 8 nel passaggio *i* ° di Newton-Raphson, la stima successiva ![ Mostra le variabili per la stima successiva.](images/cdmp-image133.png) viene ottenuto dalla formula:

![Mostra la formula per la stima.](images/cdmp-image135.png)

L'iterazione si interrompe quando l'errore (distanza nello spazio CIELUV) è inferiore a un livello di tolleranza preimpostato (0,1 nella CTE) o quando il numero di iterazioni ha superato il numero massimo consentito di iterazioni (10 nella CTE). I valori per la tolleranza e il numero di iterazioni sono stati determinati in modo empirico come validi. Nelle versioni future, il valore di tolleranza può essere modificato.

La matrice jacobiano viene calcolata usando la differenza in avanti, tranne che in corrispondenza di un punto limite (uno o più dei R, G, B è 1) in cui viene invece usata la differenza tra le versioni precedenti. Invece di calcolare l'inverso della matrice jacobiano, il sistema lineare viene risolto direttamente usando Gauss-Jordan l'eliminazione con l'intera trasformazione pivot.

Alla fine delle iterazioni, è possibile che la convergenza non venga comunque eseguita perché Newton-Raphson è un algoritmo "locale", ovvero funziona correttamente se si inizia con una supposizione iniziale vicina alla soluzione vera e propria. Se, alla fine del Newton-Raphson iterazioni, la convergenza entro la tolleranza di errore predefinita non è stata realizzata, le iterazioni vengono riavviate con un nuovo set di semi, definito come segue.

Ad esempio, la soluzione migliore ottenuta finora è (r, g, b). Da questa soluzione vengono derivati i semi a posteriori, dove N = 4. In modo intuitivo, la soluzione viene spostata "verso il centro" in una dimensione del passaggio che dipende da N. Vedere la figura 6.

![Diagramma che mostra le direzioni di perturbazione della soluzione.](images/cdmp-image136.png)

**Figura 6** : la direzione di perturbazione della soluzione dipende da quale ottetto si trova in.

In altre parole, se r &gt; 0,5, il valore sul canale r viene ridotto; in caso contrario, il valore viene aumentato. Esiste una logica simile per i canali G e B. Le definizioni esatte sono:

PERTURBATION = 0,5/(N + 1)

Dir (r) =-1 se r &gt; 0,5; + 1 in caso contrario. In modo analogo per dir (g) e dir (b)

Il valore di inizializzazione di JTH a posteriori, s????, è (r + dir (r) j Perturbation \* \* , g + dir (g) j Perturbation \* \* , b + dir (b) \* j \* Perturbation)

Prova la prima s???? e se fornisce una nuova soluzione entro la tolleranza di errore, è possibile arrestare. In caso contrario, provare la seconda s???? e così via fino all'ennesimo????.

Le schematiche dell'intero algoritmo sono illustrate nella figura 7.

![Diagramma che mostra il flusso per l'inversione del modello di dispositivo.](images/cdmp-image138.png)

**Figura 7** : schemi di inversione del modello di dispositivo

### <a name="rgb-virtual-device-model-baseline"></a>Linea di base del modello di dispositivo virtuale RGB

Questo modello di dispositivo (DM) è un semplice algoritmo di riproduzione a matrice/tono. La matrice viene derivata dal punto bianco e dalle primarie usando gli algoritmi di scienza dei colori standard. La curva di riproduzione del tono è derivata dai parametri di misurazione in base alle descrizioni ICC di CurveType e ParametricType (o invertite in base alle esigenze). I dettagli degli algoritmi interni verranno forniti dopo la convalida aggiuntiva di problemi di intervallo dinamico elevato.

Il modello di dispositivo virtuale RGB è una curva di riproduzione a matrice/tono idealizzata RGB simile alla progettazione del profilo basato su matrice di tre componenti di ICC. I parametri di "misurazione virtuale" del DM includono un valore di punto bianco (CIE XYZ assoluto), i valori primari RGB (CIE XYZ assoluti) e una curva di riproduzione del tono basata sulle ParametricCurveType ICC e CurveType in formato XML coerenti con gli schemi DMP.

La tabella seguente illustra la codifica del tipo di funzione ICC parametricCurveType e il supporto corrispondente in IRGBVirtualDeviceModelBase.



| Tipo di funzione                                         | Parametri                          | Tipo                                     | Nota                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Mostra la funzione ' GammaType '.](images/cdmp-image154.png)<br/> | g<br/>              | GammaType<br/>                 | Implementazione comune<br/>           |
| ![Mostra la funzione ' GammaOffsetGainType '.](images/cdmp-image156.png)<br/> | GA b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Mostra la funzione ' GammaOffsetGainOffsetType '.](images/cdmp-image158.png)<br/> | GA b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Mostra la funzione ' GammaOffsetGainGainType '.](images/cdmp-image160.png)<br/> | GA b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> sRGB<br/> |
| ![Mostra una funzione per i parametri ' g a b c d e f '.](images/cdmp-image162.png)<br/> | GA b c d e f<br/>   | N/D<br/>                       | Non supportato in WCS<br/>            |



 

La curva di tono per i dispositivi virtuali RGB viene applicata in DeviceToColorimetric tra i dati di input, pDeviceColors e la moltiplicazione della matrice. Per ColorimetricToDevice, è necessario usare un metodo per invertire la curva di tono. Nell'implementazione di base questa operazione viene eseguita dall'interpolazione diretta nella stessa curva di tono utilizzata per DeviceToColorimetric.

Le curve devono essere specificate nei profili come coppie di numeri nello spazio float. Il primo numero rappresenta i valori in pDeviceColors. Il secondo numero rappresenta l'output della curva di tono. Tutti i valori nella curva di tono devono essere compresi tra minColorantUsed e maxColorantUsed. Le curve di tono devono contenere almeno due voci, una per minColorantUsed e una per maxColorantUsed. Il numero massimo di voci in ToneCurve è 2048. In generale, maggiore è il numero di voci nella tabella, più accuratamente è possibile modellare la curvatura. Viene eseguita un'interpolazione lineare a tratti tra le voci.

È possibile considerare metodi di interpolazione alternativi. Se si conosce qualcosa sul comportamento sottostante del dispositivo, è possibile usare un minor numero di campioni e un modello più accurato con una curva di ordine superiore. Tuttavia, se si usa il tipo di curva errato, sarà molto impreciso. Senza ulteriori informazioni, non è possibile indovinare il tipo di curva. Quindi, usare l'interpolazione lineare e fornire molti punti dati.

### <a name="cmyk-printer-device-model-baseline"></a>Baseline modello di dispositivo stampante CMYK

Una descrizione del dispositivo di una stampante CMYK è costituita dalla creazione di un modello empirico del dispositivo che prevede il colore stampato per un determinato valore CMYK. La caratterizzazione include anche l'inversione di questo modello, in modo che sia possibile assegnare una prescrizione del valore CMYK a noi per un determinato colore. Questa operazione viene in genere definita in termini di valore di CIE XYZ o CIELAB.

In genere, viene usata una destinazione IT 8,7/3 contenente le patch CMYK. Le patch sono costituite dal campionamento dello spazio CMYK in modo ben definito in modo da formare una griglia rettangolare (con spaziatura non uniforme in C, M, Y e K). Ogni patch viene quindi misurata con un colorimetro o uno spettrofotometro. Le misurazioni nei valori CIE XYZ formano quindi una tabella di ricerca (LUT), da cui viene compilato un modello empirico della stampante usando il metodo di interpolazione di Sakamoto. US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[ 1 \] . I due brevetti citati sono scaduti.

I requisiti specifici per gli esempi di misurazione CMYK necessari per l'accettazione di un profilo del modello di dispositivo come validi dal modello di dispositivo Baseline Printer CMYK sono i seguenti. Il set di esempi è descritto più chiaramente come un set di cubi di esempio CMY, ognuno associato a un livello K specifico.

-   È necessario fornire almeno cubi CMY validi per i livelli K = 0 e K = 100.
-   È possibile che i livelli intermedi K non siano distanziati in modo uniforme.
-   Qualsiasi livello intermedio K senza un cubo CMY valido verrà ignorato.
-   I cubi CMY possono usare intervalli di campionamento non uniformi (spaziatura della griglia), ma lo stesso set di intervalli di campionamento deve essere usato in tutte le dimensioni C, M e Y del cubo CMY per un determinato livello K.
-   Ogni cubo CMY di livello K può usare un numero e una spaziatura diversi di intervalli di campionamento.
-   Tutti i cubi CMY devono contenere gli "angoli" del cubo CMY, ovvero i campioni CMY a \[ 0, 0, 0 \] , \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .
-   Tutti i livelli di griglia CMY intermedi devono essere campionati in modo completo in ogni canale. In altre parole, un campione deve esistere in ogni intersezione di griglia 3D all'interno del cubo CMY.
-   Per i cubi K = 0 e K = 100 CMY, i Cubi 2x2x2 "solo gli angoli" sono i cubi minimo accettati come validi.

    \[Nota: per K = 0 e K = 100 livelli, un cubo 3x3x3 CMY verrà elaborato come un cubo 2x2x2 "solo angoli"; il livello di campionamento intermedio viene ignorato. in 4x4x4 e nei cubi più grandi saranno usati tutti gli esempi in griglia.\]

-   Per i livelli intermedio K, i cubi 4x4x4 CMY sono i cubi minimo accettati come validi.

Un profilo di qualità elevata utilizzerà griglie di campionamento più sottili del valore minimo necessario per la validità, in genere 9x9x9x9 o versione successiva. Gli esempi di IT 8.7/3, IT 8,7/4 e ECI targets producono i profili dei modelli di dispositivo (DMPs) validi per il modello di dispositivo Baseline della stampante CMYK. Sebbene questo modello di dispositivo sia in grado di ignorare gli esempi estranei (fuori griglia) in queste destinazioni, non è garantito che sia possibile eseguire questa operazione per altre destinazioni, quindi è consigliabile rimuovere gli esempi estranei dai set di misure che passano ai profili per questo modello di dispositivo.

L'inversione del modello di stampante presenta maggiori difficoltà. Dato un colore di input in CIECAM, si verifica se questo colore si trova all'interno del gamut della stampante. Esiste anche il problema relativo alla disposizione dei punti nello spazio di aspetto dei colori. Sebbene sia possibile disporre i valori CMYK in modo che rientrino in una griglia rettangolare, come avviene nella destinazione 8,7/3, lo stesso non può essere detto dei colori stampati risultanti perché si trovano nello spazio di aspetto del colore. In generale, sono sparse nello spazio di aspetto dei colori senza motivo particolare.

Esistono in genere due approcci al problema di inversione dei punti sparsi. Un approccio consiste nell'usare una suddivisione geometrica della gamma di stampanti usando solidi tridimensionali primari, ad esempio tetraedri. Una suddivisione del gamut della stampante nello spazio di aspetto dei colori può essere indotta dalla suddivisione corrispondente dello spazio CMY (K), vedere Hung \[ 93 \] , Kang \[ 97 \] . Questo approccio offre il vantaggio della semplicità computazionale. Nel caso di un tetraedro, solo quattro punti vengono usati in un'interpolazione. D'altra parte, il risultato dipende molto da alcuni punti, il che significa che un errore di misurazione avrà un effetto significativo sul risultato. L'interpolatore tende anche a non essere uniforme. Il secondo approccio non presuppone alcuna suddivisione ed è basato sulla tecnica di interpolazione dei dati sparsi. Un esempio classico è la tecnica dell'interpolazione di Shepard o del metodo ponderato inverso (vedere Shepard \[ 68 \] ). In questo caso, diversi punti che racchiudono il punto di input vengono scelti in qualche modo, ognuno assegna un peso, generalmente proporzionale alla distanza e l'interpolazione viene considerata come la media ponderata dei punti adiacenti. In questo approccio, la scelta dei punti adiacenti è fondamentale per le prestazioni. Sebbene un numero troppo basso di punti possa rendere l'interoperabilità non accurata e non smussata, troppi punti impongono un elevato costo computazionale, in quanto i pesi sono in genere funzioni non lineari e costose da calcolare.

I due approcci descritti in precedenza presentano problemi. L'approccio di suddivisione dipende dal fatto che i dati siano ragionevolmente privi di rumore e, in genere, l'interpolazione non è molto semplice. L'interpolazione dei dati sparse è più tollerante al rumore dei dati e in genere fornisce un'interpolazione più uniforme, ma è più costosa dal punto di vista del calcolo.

La nuova CTE accetta un approccio alternativo. Il dispositivo CMYK viene considerato come una raccolta di diversi dispositivi CMY, ognuno dei quali ha un valore specifico di nero (K). Usando un algoritmo di selezione che accetta come parametri luminosità e Chroma, viene scelto un livello di nero. I valori CMY vengono ottenuti dall'inversione della tabella CMY corrispondente alla tabella Luv usando i metodi Newton usati altrove dall'algoritmo di stampa RGB.

Seguire questa procedura.

1.  Stampare la destinazione di caratterizzazione, ovvero la destinazione 8.7/3, oppure una destinazione contenente il campionamento dello spazio CMYK a intervalli regolari o irregolari.
2.  Misurare la destinazione usando uno spettrofotometro e convertire le misurazioni nello spazio CIELUV.
3.  Costruire la mappa in diretta da CMYK a Luv.
4.  Usare la mappa in linea per costruire un set di CMY a Luv Maps per un intervallo di valori K.
5.  Per qualsiasi valore di input Luv, il valore CMYK corrispondente viene ottenuto selezionando una delle mappe costruite nel passaggio 4 precedente e invertendo l'uso del metodo di Newton per ottenere un set di colori CMY associato al valore K selezionato.

I passaggi 1 e 2, ovvero le procedure standard, vengono eseguiti da un programma di profilatura che non fa parte della nuova CTE. La destinazione IT 8,7/3 contiene un campionamento ragionevolmente dettagliato di tutti i valori CMYK a diversi livelli di C, M, Y e K. in alternativa, è possibile usare una destinazione personalizzata con campionamento uniforme dei canali C, M, Y e K. Dopo la stampa della destinazione, è possibile usare uno spettrofotometro o un colorimetro per misurare il valore XYZ di ogni patch e il valore XYZ può essere convertito nel valore Luv usando il modello CIELUV.

Passaggio 3: la costruzione della mappa in avanti da CMYK a Luv può essere realizzata applicando qualsiasi tecnica di interpolazione nota, ad esempio tetraedrica o metodo multilineare, sulla griglia rettangolare nello spazio CMYK. Nella nuova CTE viene utilizzata un'interpolazione tetraedrica a 4 dimensioni. Poiché le griglie di campionamento CMY sono generalmente diverse a seconda del livello K, tuttavia, viene usata una tecnica di supercampionamento, come descritto di seguito. Per un determinato punto CMYK, i livelli sandwich K vengono innanzitutto determinati in base al valore K. Introdurre quindi una "Supergrid" a ogni livello K che rappresenta un'Unione delle griglie CMY in ognuno dei due livelli K. A ogni livello K, il valore Luv di qualsiasi punto di griglia appena introdotto viene ottenuto da un'interpolazione tetraedrica tridimensionale all'interno del livello K. Infine, in questa nuova griglia viene eseguita un'interpolazione tetraedrica a 4 dimensioni per il punto CMYK specifico.

![Diagramma che mostra il sovracampionamento.](images/cdmp-image163.png)

**Figura 8** : supercampionamento

Il passaggio 4 costruisce un set di tabelle di ricerca da CMY a Luv (LUTs). La mappa in avanti costruita nel passaggio 3 viene chiamata ripetutamente per ricampionare lo spazio CMYK. Lo spazio dei colori CMYK viene campionato usando una spaziatura uniforme di K e un campionamento di CMY diverso, ma ancora in modo uniforme.

Il passaggio 5 è una procedura per ottenere il valore CMYK usando LUTs costruito nel passaggio 4 per qualsiasi punto di Luv di input. Viene scelto il valore appropriato di K analizzando la luminosità, nonché il grado di colore nell'Luv richiesto. Dopo aver selezionato la tabella, i valori CMY vengono ottenuti dalla tabella usando il metodo di Newton, come illustrato in precedenza nel modello di dispositivo della stampante RGB.

Lo spazio CIELUV viene usato nel modello di stampante invece che in CIEJab, perché il modello di dispositivo deve essere basato esclusivamente sui dati colorimetrico disponibili nel DMP. Il DMP contiene dati colorimetrico per ogni patch misurata, incluso il punto per i supporti, quindi è possibile convertire i dati CIE XYZ in dati CIELUV. Tuttavia, non è possibile eseguire la conversione in CIECAM02 JCh o jab, perché non è possibile accedere alle informazioni sulla condizione di visualizzazione nel DMP.

### <a name="rgb-projector-device-model-baseline"></a>Baseline modello di dispositivo proiettore RGB

Nota: molti proiettori RGB hanno più di una modalità operativa. In una modalità, che è spesso l'impostazione predefinita e potrebbe essere chiamata come "presentazione", la risposta al colore del proiettore è ottimizzata per la massima luminosità. Tuttavia, in questa modalità, il proiettore perde la possibilità di riprodurre colori chiari, leggermente cromatici, ad esempio i gialli pallidi e alcuni toni di carne. In un'altra modalità, spesso denominata "film", "video" o "sRGB", il proiettore è ottimizzato per la riproduzione di immagini realistiche e scene naturali. In questa modalità, la luminosità massima viene comunicata per migliorare la qualità complessiva della riproduzione dei colori. Per ottenere una riproduzione dei colori soddisfacente con i proiettori RGB, è necessario posizionare il proiettore in una modalità in cui è possibile riprodurre una gamma uniforme di colori.

![Diagramma che mostra un modello di dispositivo D L P.](images/cdmp-image167.png)

**Figura 9** : modello di dispositivo DLP

Un valore RGB in ingresso passa attraverso due percorsi computazionali. Il primo è il modello Matrix, che restituisce un valore XYZ. Questa operazione è seguita immediatamente dalla conversione da XYZ a Luv. Il secondo è l'interpolazione LUT non uniforme mediante l'interpolazione di tetraedrica. L'output dell'interpolazione si trova già nello spazio Luv per costruzione. Per ottenere il valore Luv stimato vengono aggiunti i due output. Viene infine convertito in XYZ, ovvero l'output previsto del modello colorimetrico per il dispositivo DLP.

Poiché i proiettori sono dispositivi di visualizzazione, supportano anche l'inversione del modello, ovvero la trasformazione da XYZ a RGB. Poiché il modello di dispositivo trasforma lo spazio RGB nello spazio XYZ, che sono entrambi tridimensionali, l'inversione è equivalente alla risoluzione di tre equazioni non lineari in tre incognite. Questa operazione può essere eseguita dalle tecniche standard di risoluzione delle equazioni, ad esempio Newton-Raphson. È preferibile, tuttavia, convertire prima XYZ in Luv, quindi invertire il Luv nella trasformazione RGB, perché lo spazio Luv è più percettivamente lineare dello spazio XYZ.

### <a name="icc-device-model-baseline"></a>Baseline del modello di dispositivo ICC

L'interoperabilità del flusso di lavoro ICC viene abilitata mediante la creazione di un profilo del modello di dispositivo di baseline del dispositivo ICC speciale che archivia l'oggetto profilo e crea una trasformazione ICC usando un profilo no-op XYZ. Questa trasformazione viene quindi utilizzata per la conversione tra i colori del dispositivo e del CIE XYZ.

![Diagramma che illustra l'interoperabilità del flusso di lavoro c I T E I c c.](images/cdmp-image168.png)

**Figura 10** : citare l'interoperabilità del flusso di lavoro ICC

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Schemi e algoritmi del sistema di colori Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





