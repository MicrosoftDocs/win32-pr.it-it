---
title: Schema e algoritmi del profilo del modello di dispositivo a colori WCS
description: In questo argomento vengono fornite informazioni sullo schema del profilo del modello di dispositivo a colori WCS e sugli algoritmi associati. Questo argomento contiene le sezioni seguenti OverviewColor Device Model Profile ArchitectureThe CDMP SchemaWCS CDMP v2.0 Calibration AdditionThe CDMP Schema ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTypeMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe  Algoritmi di base CDMPResotto di base del modello di dispositivo CDMP Baseline Modello di dispositivoLCD BaselineRGB Modello di dispositivo stampante BaselineRGB Modello di dispositivo virtuale Baseline del modello di dispositivo della stampanteCmyk Modello di dispositivo BaselineRGB Modello di dispositivo Baseline del dispositivoCC Baseline del modello di dispositivoICC Argomenti correlati
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Windows Sistema colori (WCS), profilo modello di dispositivo a colori (CDMP)
- WCS (Windows Color System),profilo modello di dispositivo a colori (CDMP)
- gestione dei colori delle immagini, profilo del modello di dispositivo a colori (CDMP)
- gestione dei colori, profilo del modello di dispositivo a colori (CDMP)
- colori, profilo modello di dispositivo a colori (CDMP)
- Windows Sistema colori (WCS), profili
- WCS (Windows Color System),profiles
- gestione dei colori delle immagini, profili
- gestione dei colori, profili
- colori, profili
- schemi, profilo modello di dispositivo a colori (CDMP)
- algoritmi, profilo modello di dispositivo a colori (CDMP)
- profilo modello di dispositivo a colori (CDMP)
- CDMP (profilo del modello di dispositivo a colori)
- Profilo del modello di dispositivo a colori WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210da85cd320a80e6b29a59e3cb5ff37c86fd174934832404e4b52cf53bd110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118037900"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>Schema e algoritmi del profilo del modello di dispositivo a colori WCS

In questo argomento vengono fornite informazioni sullo schema del profilo del modello di dispositivo a colori WCS e sugli algoritmi associati.

In questo argomento sono incluse le sezioni seguenti:

-   [Overview](#overview)
-   [Architettura del profilo del modello di dispositivo a colori](#color-device-model-profile-architecture)
-   [The CDMP Schema](#the-cdmp-schema)
-   [Aggiunta di calibrazione WCS CDMP v2.0](#wcs-cdmp-v20-calibration-addition)
-   [Elementi dello schema CDMP](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [Versione spazio dei nomi](#namespaceversion)
    -   [Version](#namespaceversion)
    -   [Documentazione](#documentation)
    -   [Elemento CRTDevice](#crtdevice-element)
    -   [Elemento LCDDevice](#lcddevice-element)
    -   [Elemento ProjectorDevice](#projectordevice-element)
    -   [Elemento ScannerDevice](#scannerdevice-element)
    -   [CameraDevice - elemento](#cameradevice-element)
    -   [RGBPrinterDevice - elemento](#rgbprinterdevice-element)
    -   [Elemento CMYKPrinterDevice](#cmykprinterdevice-element)
    -   [RGBVirtualDevice - elemento](#rgbvirtualdevice-element)
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
    -   [Tipo di geometria](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeCMYKSampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeCMYKType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [Extensiontype](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [Algoritmi di base CDMP](#the-cdmp-baseline-algorithms)
    -   [Baseline del modello di dispositivo CRT](#crt-device-model-baseline)
    -   [Baseline del modello di dispositivo LCD](#lcd-device-model-baseline)
    -   [Linea di base del modello di dispositivo della stampante RGB](#rgb-printer-device-model-baseline)
    -   [Baseline del modello di dispositivo virtuale RGB](#rgb-virtual-device-model-baseline)
    -   [Linea di base del modello di dispositivo della stampante CMYK](#cmyk-printer-device-model-baseline)
    -   [Baseline del modello di dispositivo del proiettore RGB](#rgb-projector-device-model-baseline)
    -   [Baseline del modello di dispositivo ICC](#icc-device-model-baseline)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Questo schema viene usato per specificare il contenuto di un profilo cdMP (Color Device Model Profile). Gli algoritmi di base associati sono descritti di seguito.

Lo schema del profilo del modello di dispositivo (DMP) di base è costituito dai dati di misurazione del campionamento.

Il componente di campionamento dell'XML Schema DMP fornisce il supporto per le destinazioni di misurazione dei colori di base, concentrandosi su destinazioni standard comuni e destinazioni ottimizzate per i modelli di dispositivo di base.

Inoltre, il profilo del dispositivo fornisce informazioni specifiche sul modello di dispositivo di destinazione e fornisce un criterio che il modello di dispositivo di fallback di base può usare se il modello di destinazione non è disponibile. Le istanze del profilo possono includere estensioni private tramite meccanismi di estensione XML standard.

## <a name="color-device-model-profile-architecture"></a>Architettura del profilo del modello di dispositivo a colori

![Diagramma che mostra le informazioni che costituisce un profilo del modello di dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>The CDMP Schema


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



## <a name="wcs-cdmp-v20-calibration-addition"></a>Aggiunta di calibrazione WCS CDMP v2.0

**L'elemento ColorDeviceModel** dello schema CDMP è stato aggiornato in Windows 7 per includere il nuovo elemento di calibrazione. Di seguito viene illustrata la modifica dello schema CDMP.


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
> Le primarie sono esempi principali di rosso, verde, blu, nero e bianco. Una rampa primaria è una rampa tonale dalla minima luminance al valore primario completo. Il numero massimo di voci in una rampa di tono è 4096.

 

> [!Note]  
> Le dmp devono avere dati di misurazione.

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

Questo elemento è di tipo ColorDeviceModel.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="colordevicemodel"></a>ColorDeviceModel

Questo elemento è una sequenza dei sotto-elementi seguenti

1.  Stringa ProfileName,
2.  facoltativo Descrizione stringa,
3.  stringa author facoltativa,
4.  facoltativo MeasurementConditions MeasurementConditionsType,
5.  Self-Luminous booleano,
6.  MaxColorant float,
7.  MinColorant float,
8.  Scelta degli elementi
    1.  CRTDevice,
    2.  LCDDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. ExtensionType facoltativo

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo. Gli elementi secondari della stringa hanno un massimo di 10.000 caratteri. Il sotto-elemento MaxColorant deve essere maggiore o uguale a zero (0) e maggiore del sotto-elemento MinColorant. MinColorant può essere negativo.

### <a name="namespaceversion"></a>Versione spazio dei nomi

xmlns:cdm=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Versione

Versione = "1.0" con Windows Vista.

**Condizioni di convalida:** Qualsiasi valore di &gt; versione 0.1 o =2.0 è valido per &lt; supportare modifiche non di rilievo al formato.

### <a name="documentation"></a>Documentazione

Schema del profilo del modello di dispositivo.

Copyright (C) Microsoft. Tutti i diritti sono riservati.

### <a name="crtdevice-element"></a>Elemento CRTDevice

Questo elemento è una sequenza di sotto-elementi di measurementData DisplayMeasurementType.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="lcddevice-element"></a>Elemento LCDDevice

Questo elemento è una sequenza di sotto-elementi di measurementData DisplayMeasurementType.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="projectordevice-element"></a>Elemento ProjectorDevice

Questo elemento è una sequenza di sotto-elementi di measurementData RGBProjectorMeasurementType.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="scannerdevice-element"></a>Elemento ScannerDevice

Questo elemento è una sequenza di sotto-elementi di measurementData RGBCaptureMeasurementType

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="cameradevice-element"></a>CameraDevice - elemento

Questo elemento è una sequenza di sotto-elementi di measurementData RGBCaptureMeasurementType

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="rgbprinterdevice-element"></a>RGBPrinterDevice - elemento

Questo elemento è una sequenza di sotto-elementi di measurementData RGBPrinterMeasurementType.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="cmykprinterdevice-element"></a>Elemento CMYKPrinterDevice

Questo elemento è una sequenza di sotto-elementi di measurementData CMYKPrinterMeasurementType.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="rgbvirtualdevice-element"></a>RGBVirtualDevice - elemento

Questo elemento è una sequenza di sotto-elementi di RGBVirtualMeasurementDataType.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="plugindevicetype"></a>PlugInDeviceType

Questo elemento è una sequenza di un GUID GUIDType ed eventuali sotto-elementi.

**Condizioni di convalida:** Il GUID viene usato per trovare la corrispondenza con il GUID dll plugin dm. Esistono un massimo di 100.000 sotto-elementi secondari personalizzati.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Questo elemento è una sequenza costituita da

1.  Gruppo RGBPrimariesGroup
2.  Scelta di
3.  -   Gamma
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   Elementi ToneResponseCurves

4.  facoltativo GamutBoundarySamples GamutBoundarySamplesType
5.  TimeStamp dateTime

**Condizioni di convalida:** Ogni sotto-elemento di questi tipi ha le proprie condizioni di convalida.

### <a name="gammatype"></a>GammaType

Questo elemento è un tipo complesso costituito dall'attributo

-   Gamma NonNegativeFloatType

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Questo elemento è un tipo complesso costituito dagli attributi

-   Gamma NonNegativeFloatType
-   Offset NonNegativeFloatType
-   Gain NonNegativeFloatType

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Questo elemento è un tipo complesso costituito dagli attributi

-   Gamma NonNegativeFloatType
-   Offset NonNegativeFloatType
-   Gain NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Questo elemento è una sequenza di

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

L'elemento ha anche un attributo TRCLength di tipo unsignedint.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Questo elemento è una sequenza di RGBType RGB.

**Condizioni di convalida:** Frequenze massime attualmente illimitate, da inviare in base ai commenti e suggerimenti del settore.

### <a name="floatpairlist"></a>FloatPairList

Questo elemento è un tipo semplice di elenco di coppie di valori float.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

Questo elemento è un

1. sequenza dell'elemento ColorCube costituita da una sequenza di Sample NonNegativeCMYKSampleType

2. Attributo dateTime di TimeStamp.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Questo elemento è un

1. sequenza di elemento ColorCube costituita da una sequenza di Sample NonNegativeRGBSampleType

2. Attributo dateTime di TimeStamp.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Questo elemento è una sequenza di

1.  complexType PrimaryIndex di
2.  1.  White OneBasedIndex
    2.  OneBasedIndex nero facoltativo
    3.  OneBasedIndex rosso facoltativo
    4.  Facoltativo OneBasedIndex verde
    5.  Facoltativo OneBasedIndex blu
    6.  Facoltativo Cyan OneBasedIndex
    7.  Facoltativo Magenta OneBasedIndex
    8.  Facoltativo OneBasedIndex giallo

3.  NeutralIndices delle righe di OneBasedIndex
4.  Sequenza ColorSamples di Sample NonNegativeRGBSampleType

L'elemento ha anche un attributo dateTime TimeStamp.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="onebasedindex"></a>OneBasedIndex

Questo elemento è un tipo semplice di restrizione base unsigned int con valore minInclusive = "1".

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Questo elemento è una sequenza di

1.  Gruppo RGBPrimariesGroup
2.  elemento ColorSamples costituito dalla sequenza di Sample NonNegativeRGBSampleType

L'elemento ha anche un attributo dateTime TimeStamp.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Questo elemento è una sequenza di

1.  group RGBPrimariesGroup
2.  GrayRamp della sequenza di Sample NonNegativeRGBType
3.  RedRamp della sequenza di Sample NonNegativeRGBType
4.  GreenRamp della sequenza di Sample NonNegativeRGBType
5.  BlueRamp della sequenza di Sample NonNegativeRGBType

L'elemento DisplayMeasurementType ha anche un attributo dateTime TimeStamp.

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

MeasurementConditionsType è una sequenza di sotto-elementi che contiene:

1.  Valore di enumerazione delle stringhe con restrizioni ColorSpace "CIEXYZ"
2.  Scelta facoltativa dell'enumerazione di stringhe WhitePoint NonNegativeXYZType o WhitePointName dei valori D50, D65, A o F2
3.  Geometry GeometryType
4.  Valore intero ApertureSize in millimetri

I valori predefiniti sono:

1.  Stampanti RGB e CMYK:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  ApertureSize 10mm
2.  Scanner:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  ApertureSize 10mm
3.  Display e dispositivo virtuale RGB:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  0/45 GeometryType
    4.  ApertureSize 10mm
4.  Telecamere:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  GeometryType diretto
    4.  ApertureSize 10mm

**Condizioni di convalida:** La convalida di ogni sotto-elemento è determinata dalle condizioni di convalida per tali sotto-elementi. Se manca un sotto-elemento, viene usato il valore predefinito specifico del tipo di modello di dispositivo.

### <a name="geometrytype"></a>Tipo di geometria

string

Valori di enumerazione:

-   "0/45"
-   "0/diffuse"
-   "diffuse/0"
-   "Diretto"

**Condizioni di convalida:** Qualsiasi valore ad eccezione dei valori di numerazione elencati non è valido. Queste informazioni non modificheranno il comportamento di elaborazione della baseline.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Questo elemento è una sequenza di

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="nonnegativecmyksampletype"></a>NonNegativeCMYKSampleType

Questo elemento è una sequenza di

1.  CMYK NonNegativeCMYKType
2.  CIEXYZ NonNegativeXYZType

L'elemento ha anche una stringa tag di attributo facoltativa

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Questo elemento è una sequenza di

1.  RGB NonNegativeRGBType
2.  CIEXYZ NonNegativeXYZType

L'elemento ha anche una stringa tag di attributo facoltativa

**Condizioni di convalida:** Da determinare in base ai commenti e suggerimenti del settore.

### <a name="nonnegativecmyktype"></a>NonNegativeCMYKType

Questo elemento è costituito da attributi

1.  C float
2.  M float
3.  Y float
4.  K float

**Condizioni di convalida:** Da determinare dai commenti e suggerimenti del settore.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Questo elemento è costituito da attributi

1.  Float R
2.  G float
3.  B float

**Condizioni di convalida:** Da determinare dai commenti e suggerimenti del settore.

### <a name="extensiontype"></a>Extensiontype

L'elemento ExtensionType è una sequenza di qualsiasi tipo di sotto-elemento e viene usato per informazioni proprietarie da applicazioni non Microsoft.

**Condizioni di convalida:** Questo elemento è facoltativo. Possono essere presenti al massimo 1000 elementi secondari dell'estensione.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

L'elemento NonNegativeXYZType è costituito da tre elementi A virgola mobile IEEE a precisione singola denominati "X", "Y" e "Z". Questi valori sono limitati ai valori di misura dei profili DMP. Queste misurazioni possono essere valori assoluti (non relativi) CIEXYZ 1931 riflettenti o valori assoluti (non relativi) CIEXYZ 1931 diretti (trasmissivi) in candela per unità quadrate del contatore.

**Condizioni di convalida:** Sono validi solo i valori reali e i valori di misura CIEXYZ negativi non sono validi. Poiché si tratta di valori assoluti, i valori possono essere maggiori di 1,0f. Limite ragionevole per qualsiasi "X", "Y" o "Z". value è arbitrariamente impostato su 10000.0f.

### <a name="xyztype"></a>XYZType

L'elemento XYZType è costituito da tre valori a virgola mobile IEEE a precisione singola: "X", "Y" e "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Algoritmi di base CDMP

### <a name="crt-device-model-baseline"></a>Baseline del modello di dispositivo CRT

Per comprendere questo modello, è necessario considerare sia il processo di caratterizzazione che la modellazione dei dispositivi. Nel processo di caratterizzazione, le misurazioni XYZ vengono eseguite per la prima volta sui colori ottenuti riempiendo il buffer di visualizzazione di un dispositivo di visualizzazione CRT. I valori di esempio seguenti genereranno dati validi per il modello di dispositivo CRT di base:

Rosso: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blu: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrali: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

È anche possibile usare incrementi diversi da 15 e incrementi non lineari. Ogni rampa rossa, verde, blu e neutra deve contenere almeno tre campioni, ma è consigliabile fornire altri esempi. È necessario fornire esempi per rosso, verde, blu, nero e bianco puro. Non è necessario che gli esempi siano spaziati in modo uniforme.

Il processo di compilazione della matrice tristimulus è costituito da due passaggi. Per prima cosa, stimare il valore XYZ del punto nero o il flare. Questo passaggio si basa principalmente sul lavoro di Berns 3 con una funzione obiettivo leggermente modificata \[ \] per l'ottimizzazione non lineare. In secondo piano, calcolare la matrice tristimulus in base al risultato del primo passaggio e anche da un calcolo della media su tutte le misurazioni per canale, non solo su quella per il numero massimo di dati digitali.

Ognuno di questi passaggi contiene procedure dettagliate. Il punto di partenza sono le rampe (17 passaggi nell'esempio) per ognuno dei canali R, G e B. Quando le misure XYZ vengono tracciate sul piano *xy* della cromaticità, nella figura 1 viene illustrata una situazione tipica. Il primo passaggio consiste nella risoluzione di un problema di ottimizzazione non lineare per trovare il punto nero "best fit" che ridurrà al minimo la deriva nella cromaticità quando si attraversano i canali R, G e B. In base a Berns \[ \] 3, si cerca ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z <sub>K</sub>* ) che riduce al minimo la funzione obiettivo seguente:

![Mostra la funzione obiettivo in cui Sr, Sg e Sb sono il set di punti dati sui canali R, G e B.](images/cdmp-formula1.png)

dove *S <sub>R,</sub>**S <sub>G</sub>* e *S <sub>B</sub>* sono il set di punti dati corrispondenti ai punti sui canali R, G e B. Per qualsiasi set *S* definire:

![Mostra una formula per definire qualsiasi set S.](images/cdmp-formula2.png)

Nel precedente, \| *S* \| è la cardinalità di *S*, ad esempio il numero di punti nel set S . ![ Mostra una formula per la cromaticità di un punto.](images/cdmp-formula3.png) è le coordinate di cromaticità del punto ![ Mostra una formaula per un punto.](images/cdmp-formula4.png) , quindi Mostra una formula per la media o il centro della massa. , è la media, o il centro della massa, di tutti i punti del set S nel piano ![ ](images/cdmp-formula5.png) di cromaticità.  Mostra quindi ![ una formula per la somma di un secondo istante di punti.](images/cdmp-formula6.png) è la somma dei secondi momenti dei punti relativi al centro della massa ed è una misura della distribuzione dei punti. Infine, ![ mostra una formula per la misura totale della distribuzione di tre cluster di punti.](images/cdmp-formula7.png) è una misura totale della distribuzione dei tre cluster di punti sui rispettivi centri di massa.

Nel calcolo di ![ Mostra una formula di f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png) , se ![ mostra una formula per X. , il calcolo viene ignorato e la ](images/cdmp-formula9.png) cardinalità di *S* viene modificata di conseguenza.

Nonostante l'apparente complessità della funzione obiettivo, è una somma dei quadrati di molte funzioni differenziali in *X <sub>K,</sub>**Y <sub>K</sub>Z <sub>K</sub>* (17 punti 2 *xy* -components 3 canali = 102, nell'esempio) e, di conseguenza, è utilizzabile per tecniche di minimo quadrato non lineare standard, ad esempio l'algoritmo Levenberg-Marquardt, che è l'algoritmo usato in WCS. Si noti che la funzione obiettivo precedente è diversa da quella suggerita in Berna 3, in quanto quest'ultima funzione misura la varianza delle distanze dal centro della massa, in modo che la varianza sia zero quando i punti sono \[ equidistanti dal centro della massa, anche se possono estendersi \] leggermente. Nell'esempio la dispersione dei punti viene contollata direttamente usando i secondi momenti.

Come per qualsiasi algoritmo iterativo per il problema dei quadrati meno lineari, Levenberg-Marquardt un'ipotesi iniziale. Esistono due candidati ovvi. Uno è (0, 0, 0); l'altro è il punto nero misurato. Per la CTE, il punto nero misurato viene usato per la prima volta come ipotesi iniziale. Se viene superato un massimo di 100 iterazioni senza raggiungere una soglia di una distanza media di 0,0001 di ogni punto dal centro di massa (che corrisponde a un valore soglia pari a (0,001) 17 3 = 0,000051 per la funzione obiettivo, viene eseguito un altro round di iterazioni con l'ipotesi iniziale (0, 0, 0). La stima risultante del punto nero è XYZ rispetto alla stima migliore del round precedente di iterazioni (con il punto nero misurato come ipotesi iniziale). Usare la stima che fornisce il valore più piccolo per la funzione obiettivo. La scelta di 100 iterazioni e la distanza di errore di 0,001 sono state selezionate empiricamente. Nelle versioni future potrebbe essere ragionevole parametrizzare la distanza di errore.

Il risultato del primo passaggio è il punto nero stimato ( *X <sub>K,</sub>**Y <sub>K,</sub>**Z <sub>K</sub>* ). Il passaggio 2 consiste nel determinare la matrice tristimulus mediando la cromaticità dei punti nei tre cluster ottenuti nel primo passaggio. Per i CRT, questa operazione viene eseguita principalmente per ridurre al minimo gli effetti degli errori di misurazione. I punti usati nella media della cromaticità devono essere gli stessi usati nell'ottimizzazione nel primo passaggio. In altre parole, se il primo punto (numero digitale 15, nell'esempio) in ogni rampa viene eliminato nel passaggio di ottimizzazione, è necessario eseguire la stessa operazione nella media. Se ![ mostra formule di cromaticità media per le coordinate nei canali rosso e verde.](images/cdmp-formula10.png) e ![ Mostra una formula di cromaticità media per le coordinate nel canale blu.](images/cdmp-formula11.png) sono le coordinate di cromaticità medie dei canali rosso, verde e blu, quindi la procedura seguente determina la matrice tristimulus. Prima di tutto, risolvere il sistema lineare 3?3:

![Mostra la prima parte della procedura per risolvere un sistema lineare 3?3.](images/cdmp-formula12.png)

![Mostra la seconda parte del sistema lineare 3?3.](images/cdmp-formula13.gif)![Visualizzare il valore t pscript b alla fine della seconda parte del sistema lineare 3?3.](images/cdmp-formula14.gif)

*X <sub>W,</sub>**Y <sub>W,</sub>**Z <sub>W</sub>*

![Mostra la parte finale della procedura per risolvere un sistema lineare 3?3.](images/cdmp-formula15.png)

Dopo aver determinato la matrice tristimulus, la determinazione delle curve del tono segue l'approccio standard. Per i display CRT, si presuppone che i singoli canali seguano il modello "GOG":

![Mostra la formula per il modello "G O G".](images/cdmp-formula16.png)

dove *k <sub>g</sub>* è il "guadagno", 1 -*k g <sub>è</sub>* l'"offset" e ? è il valore "gamma". La matrice inversa della matrice tristimulus viene applicata ai dati XYZ dei neutri per ottenere i dati RGB lineari, che vengono quindi correlati ai valori RGB digitali usando la regressione non lineare nel modello GOG. Queste caratteristiche non devono essere le stesse per i canali R, G e B e in genere non sono uguali.

Berns \[ \] 1: Berns, *Billmeyer e Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed. John Wiley & i figli (2000).

Berns 2: Berns e Katoh, Funzione di trasferimento da digitale a radiometrico per schermi CRT controllati dal \[ \] computer, *CIE Expert Symposium '97 Color Standards for Imaging Technology,* novembre 1997.

Berns 3: Berns, Fernandez e Taplin, Stima delle Black-Level emissioni di \[ \] Computer-Controlled Displays, Color Research and *Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)

Kang \[ \] 1: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)

Katoh 1: Katoh, Deguchi e Berns, Una descrizione accurata della proposta di monitoraggio CRT (II) per un'estensione al metodo CIE e la relativa \[ \] verifica, *Opt. Rev.* 8: 397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Baseline del modello di dispositivo LCD

La baseline del modello di dispositivo LCD è simile alla baseline del modello di dispositivo CRT. Questa sezione illustra i modi in cui la modellazione LCD differisce dalla modellazione CRT.

Una differenza è che non è possibile presupporre che i display LCD seguano il modello GOG usato per i CRT e che le curve del tono siano ottenute dall'interpolazione dei dati misurati. Per questo, l'asse neutro del dispositivo deve essere campionato più frequentemente.

Ecco alcuni valori di esempio tipici che possono generare dati validi per la baseline del modello di dispositivo LCD:

Rosso: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blu: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrali: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

Il processo di media delle cromatiche dei colori misurate per ottenere le cromatiche per le primarie dei dispositivi è più critico per le unità LCD rispetto ai CRT. Quando le misurazioni XYZ vengono tracciate sul piano *xy* della cromaticità, nella figura 1 viene illustrata una situazione tipica. Si noti come la cromaticità si sposta verso il punto nero. Ciò è dovuto al fatto che tutti i led hanno una certa quantità di perdita di luce.

![Diagramma che mostra un grafico della cromaticità usando dati non elaborati senza correzione.](images/cdmp-lcd-dmp-figure1.png)

**Figura 1:** Diagramma di cromaticità che usa dati non elaborati senza correzione

Quando viene sottratto dalle misurazioni XYZ non elaborate, nella figura 2 viene illustrata una situazione tipica. I punti sono ora raggruppati su tre centri, anche se non rientrano in modo identico. Il processo di media descritto per i CRT migliora notevolmente i risultati per i CCD.

![Diagramma che mostra un grafico della cromaticità usando dati non elaborati con un punto nero regolato.](images/cdmp-lcd-dmp-figure2.png)

**Figura 2:** Diagramma di cromaticità con dati con punto nero regolato

### <a name="rgb-capture-device-model-baseline"></a>Baseline del modello di dispositivo di acquisizione RGB

Il modello di dispositivo di acquisizione RGB di base è una sottoclasse della classe IDeviceModel. Nella caratterizzazione colorimetrica dei dispositivi di acquisizione colori, ad esempio scanner e fotocamere digitali, viene usato l'approccio seguente. Una destinazione costituita da patch di colore con valori CIEXYZ noti viene acquisita usando il dispositivo di acquisizione. Il risultato dell'acquisizione è un'immagine bitmap RGB in cui il colore di ogni patch viene codificato in un valore RGB. Questi valori RGB del dispositivo sono specifici di un particolare dispositivo di acquisizione. L'obiettivo della caratterizzazione colorimetrica è stabilire una relazione empirica tra i valori RGB del dispositivo e i valori CIEXYZ o una trasformazione matematica da RGB a XYZ che modella nel modo più accurato possibile il comportamento del dispositivo di acquisizione.

Una trasformazione matematica di questo tipo può essere modellata ragionevolmente da polinomi di gradi bassi. Questa procedura è descritta in dettaglio nella documentazione, ad esempio Kang \[ 92 \] , Kang \[ 97 \] . In Kang 97 viene segnalato un approccio che usa un set di tre \[ \] polinomi con 3, 6, 8, 9, 11, 14 o 20 termini nelle variabili R, G e B, mentre i tre polinomi regrediscono rispettivamente nei componenti X, Y, Z dello spazio CIEXYZ. Per il polinomio a 20 termini, il formato è:

![Mostra il polinomio a 20 termini.](images/cdmp-formula20.png)

Esistono espressioni simili per Y e Z. La tecnica matematica per adattare i polinomi rientra nella "regressione lineare multivariata" ed è descritta in qualsiasi testo elementare in Statistiche.

Questo metodo di regressione lineare non riduce al minimo la funzione obiettivo "giusta". Per impostazione predefinita, la regressione lineare trova la soluzione con i minimi quadrati, il che implica che i coefficienti ottenuti ridurranno al minimo la somma totale dei quadrati di errori nello spazio sottostante o, in modo equivalente, la somma dei quadrati delle distanze euclidee. In pratica, si vuole ridurre al minimo la somma dei quadrati di ? Es, dove ? E è uno degli standard accettati, ad esempio CIE94. Ridurre al minimo questa funzione obiettivo è un problema di regressione non lineare.

Nel nuovo motore, da Lab a XYZ è lo spazio colore CIE in cui viene regredita e il polinomio cubico a 20 termini viene usato come modello per il dispositivo di acquisizione, o coefficienti ls,as,bs in modo che i polinomi seguenti minimizzino la somma dei quadrati di ? E <sub>CIE94</sub> s.

![Mostra un set di formule polinomiali.](images/cdmp-formula21.png)

La soluzione ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) nello spazio numerico reale 60 **dimensionale R** 203 deve essere tale che l'errore totale seguente sia ridotto al minimo:

![Mostra l'errore totale da ridurre al minimo.](images/cdmp-formula22.png)

dove la somma è tramite tutte le coppie di punti dati (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) nel set di dati campionati e altri punti di controllo da visualizzare in dettaglio di seguito. Si tratta di un problema di regressione non lineare perché i parametri *?<sub> i</sub>*, *a <sub>i</sub>*, * <sub>i</sub>* entrano nella funzione obiettivo in modo non lineare (non quadraticamente).

Poiché la funzione obiettivo ? è una funzione non lineare (e nonquadratica) dei parametri *?<sub> i</sub>*, *a <sub>i</sub>* e * <sub>i</sub>*, è necessario ricorrere a tecniche iterative per risolvere il problema di ottimizzazione. Poiché la forma della funzione obiettivo è una somma di quadrati, viene usata una tecnica di ottimizzazione standard denominata Levenberg-Marquardt algoritmo. È considerato il metodo scelto per i problemi dei quadrati meno lineari. Per gli algoritmi iterativi, ad esempio Levenberg-Marquardt, è necessario specificare un'ipotesi iniziale. Una buona ipotesi iniziale è in genere fondamentale per trovare il valore minimo corretto. In questo caso, un buon candidato per l'ipotesi iniziale è la soluzione del problema della regressione lineare. Per prima cosa, ridurre al minimo la somma del quadrato delle distanze euclidee nello spazio lab, definendo una funzione obiettivo quadratica:

![Mostra una funzione obiettivo quadratica definita.](images/cdmp-formula23.png)

La soluzione matematica a questo problema "linear least squares" è ben nota. Perché *?<sub> i</sub>* viene visualizzato solo nella modellazione *L,* *<sub>i</sub>* viene visualizzato solo nella *modellazione u* e * <sub>i</sub>* viene visualizzato solo nella *modellazione v.* il problema di ottimizzazione può essere scomposto in tre sottoproblemi: uno per *L*, uno per *u* e uno per *v*. Si *considerino le equazioni L.* Le *equazioni u* e *le equazioni v* seguono esattamente lo stesso argomento. Il problema di ridurre al minimo la somma di quadrati di errori in *L* può essere dichiarato come risolvere l'equazione di matrice seguente nel senso dei minimi quadrati:

![Mostra un'equazione di matrice per L.](images/cdmp-formula24.png)

dove *N* è il numero totale di punti dati (punti campionati originali più punti di controllo creati nel modo descritto di seguito). In genere, *N* è molto più grande di 20, quindi l'equazione precedente è troppo determinata e richiede una soluzione con meno quadrati. Una soluzione in forma chiusa per **?** è disponibile:

![Mostra una soluzione in formato chiuso.](images/cdmp-formula25.png)

In pratica, la valutazione diretta tramite la soluzione modulo chiuso non viene usata perché ha proprietà numeriche scadente. Viene invece applicato un tipo di algoritmo di fattorizzazione della matrice alla matrice di coefficienti che riduce il sistema di equazioni in forma canonica. Nell'implementazione corrente, SVD (Singular Value Decomposition) viene applicato alla matrice **R** e quindi il sistema scomposto risultante viene risolto.

La soluzione al problema di regressione lineare, indicato da ![ Mostra la soluzione al problema di regressione lineare.](images/cdmp-formula26.png) , viene usato come punto di partenza dell'algoritmo Levenberg-Marquardt. In questo algoritmo viene calcolato un passaggio di valutazione che dovrebbe avvicinare il punto alla soluzione ottimale. Il passaggio di valutazione soddisfa un set di equazioni lineari dipendenti dal valore funzionale e dai valori dei derivati nel punto corrente. Per questo motivo, i derivati della funzione obiettivo ? rispetto ai parametri *?<sub> i</sub>*, *i <sub>i</sub> <sub>sono</sub>* input obbligatori per l'algoritmo Levenberg-Marquardt. Anche se sono presenti 60 parametri, esiste un collegamento che consente di calcolare molto meno. In base alla regola di calcolo della catena,

![Mostra un'equazione che consente un collegamento usando la regola di calcolo a catena.](images/cdmp-formula27.png)

dove *j* = 1, 2, , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* sono il valore CIELAB del punto di campionamento *i* e *R <sub>ij</sub>* è la (*i*,*j* )th entry della matrice **R** definita in precedenza. Invece di calcolare i derivati per 60 parametri, è quindi possibile calcolare i derivati *per L*,*a* e *b* usando la differenza numerica in avanti.

È anche necessario impostare un criterio di arresto per gli algoritmi iterativi. Nell'implementazione corrente le iterazioni vengono terminate se il valore di DECIE94 quadrato medio è minore di 1 o se il numero di iterazioni eseguite ha superato 10. Il numero 10 deriva dall'esperienza pratica che se le prime iterazioni non riducono in modo significativo l'errore, altre iterazioni non potrebbero essere molto utili se non spostare il punto in modo oscillatore, ad esempio l'algoritmo potrebbe non convergere. Anche nel caso in cui l'algoritmo diverga, è possibile essere certi che DECIE94 non sia peggiore di quello che è stato avviato, ad esempio con i parametri ottenuti dalla regressione lineare.

Anche con il metodo precedente di regressione non lineare, esistono diversi problemi con l'adattamento. Un problema è che i polinomi tendono a superare o sottoshoot oltre i punti dati. Nel processo di adattamento è possibile introdurre maxima e minima locali artificiali. Questa operazione può essere contrastata usando polinomie di basso grado, motivo per cui non è consigliabile usare più di tre gradi. Un aspetto più grave dell'overshooting o dell'undershooting è che, mentre un polinomio può assumere teoricamente qualsiasi valore reale, lo spazio che tenta di modellare ha in genere vincoli fisici e vincoli pratici. CIEXYZ deve avere tutti X, Y, Z non negativi, ovvero un vincolo fisico. In pratica, accettano solo valori di dimensioni di centinaia, non di migliaia o superiori. Analogamente, CIELAB o CIELUV ha vincoli fisici e pratici propri. Quando lo spazio RGB è riempito sufficientemente con punti di campionamento, il problema di overshooting o undershooting non è grave. Tuttavia, i punti RGB acquisiti dal dispositivo di acquisizione non riempiono in genere lo spazio RGB in modo uniforme. I punti possono riempirsi solo all'interno dell'80% del cubo RGB o, in caso contrario, possono risiedere in una varietà dimensionale inferiore. In questo caso, i polinomi regressi possono eseguire un'operazione non accurata nell'estrapolare i valori oltre i punti dati, talvolta restituiscono stime non realistiche. Si vuole un modello che restituisca sempre valori ragionevolmente realistici. Ciò richiede un metodo in grado di controllare in modo efficace il comportamento limite dei polinomi di regressione imponendo costi aggiuntivi ai polinomi che si comportano in modo irregolare vicino al limite del cubo RGB. Un'altra misura per garantire che i polinomi restituiranno sempre valori realistici viene applicata ritagliando l'output all'interno del locus spettrale CIE.

È a questo punto che la modellazione dello scanner e la modellazione della fotocamera divergono l'una dall'altra. Si prevede che il modello di fotocamera estrapoli in aree oltre i punti campionati, incluse le "evidenziazioni speculari", la stessa estrapolazione non è necessaria per il modello dello scanner. La destinazione dello scanner deve coprire una caratterizzazione simile ai materiali stampati da analizzare. Il modello dello scanner deve comunque essere affidabile nel senso che non deve restituire valori irrealistici, ma l'estrapolazione ben oltre la destinazione di caratterizzazione non è necessaria. Per garantire la solidità, il polinomio L precedente viene ritagliato a 100, cio' il modello polinomiale viene forzato a non estrapolare oltre "Dmin" della destinazione dello scanner.

È previsto che il modello di fotocamera estrapoli le evidenziazioni speculari, quindi il ritaglio a 100 è indesiderato. Viene invece usato l'algoritmo seguente.

Vengono introdotti punti di controllo artificiali per controllare il comportamento dei polinomi nelle aree con campionamento insufficiente. Posizionando strategicamente questi punti di controllo con i valori appropriati, servono a "tirare" i polinomi nella direzione richiesta. Nell'implementazione corrente vengono usati otto punti di controllo corrispondenti agli angoli del cubo RGB. Se i valori del dispositivo vengono normalizzati in unity, questi punti sono:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Ad eccezione del bianco *R* G B = 1, associato a un valore  =   =  CIELAB *di L* = 100, *u* v = 0, viene usato l'algoritmo di estrapolazione seguente per determinare il  =  valore CIELAB appropriato a cui associare. In genere, per un determinato (*R*,*G*,*B* ), un peso è associato a ognuno di (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) nel set di dati campionati. L'assegnazione del peso è di due obiettivi. In primo luogo, il peso è inversamente proporzionale alla distanza tra (*R*,*G*,*B* ) e (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ). In secondo piano, si vuole eliminare o assegnare il peso 0 ai punti con una tonalità diversa rispetto al punto specificato (*R*,*G*,*B* ). Per prendere in considerazione la tonalità, prendere in considerazione i punti che si trovano all'interno di un cono il cui vertice è in corrispondenza di (0, 0, 0), il cui asse coincide con l'unione della linea (0, 0, 0) a (*R*,*G*,*B* ) e il cui angolo semi-verticale ? soddisfa cos ? = 0,9. Vedere la figura 3 per un'illustrazione di questo cono.

![Diagramma che mostra la forma del quartiere.](images/cdmp-lcd-dmp-figure3.png)

**Figura 3:** Filtro dei punti di campionamento in base all'angolo e alla distanza. La forma del quartiere rappresentato è solo a scopo illustrativo. La forma effettiva dipende dalla distanza usata. è un quartiere a forma di diamante se viene usata la norma 1.

All'interno di questo cono viene eseguito un secondo filtro basato sulla distanza RGB, che usa la norma 1, definita da

![Mostra la formula per il secondo filtro all'interno del cono.](images/cdmp-formula28.png)

Con il cono corrente, la ricerca iniziale è per i punti che si trova a una distanza di 0,1 da (*R*,*G*,*B* ). Se non viene trovato alcun punto all'interno di questo raggio, il raggio viene aumentato di 0,1 e la ricerca viene riavviata. Se la rete arrotondata successiva non ha alcun punto, il raggio viene aumentato di 0,1. Questo processo continua fino a quando il raggio non supera MaxDist/5, dove MaxDist = 3, nel caso di 1 norma. Se non viene trovato alcun punto, il cono viene ingrandito diminuendo il cos ? di 0,05, cio' aumentando l'angolo? e riavviando l'intero processo con un raggio crescente. Questo processo continua fino a quando non viene trovato un set non vuoto di punti o cos ? raggiunge 0, cio' il cono si è aperto per diventare un piano. A questo punto, la ricerca viene riavviata aumentando il raggio, ad eccezione del fatto che la ricerca continua fino a quando il raggio non raggiunge MaxDist. Ciò garantisce che nello scenario peggiore, verrà trovato un set non vuoto di punti. L'algoritmo è riepilogato nel diagramma di flusso nella figura 4.

![Diagramma che mostra il flusso dell'algoritmo.](images/cdmp-lcd-dmp-figure4.png)

**Figura 4:** diagramma Flow per determinare il set S di punti di campionamento usato nell'estrapolazione per un valore RGB di input

Supponendo che il processo precedente restituisce un set non vuoto *S* di punti (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) e corrispondente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), quindi per ogni punto di questo tipo viene assegnato un peso *w <sub>i,</sub>* dato da

![Mostra la formula per un peso per ogni punto.](images/cdmp-formula29.png)

Infine, l'estrapolante è definito da

![Mostra la definizione per l'estrapolante.](images/cdmp-formula30.png)

Le equazioni precedenti costituiscono un'istanza dei "metodi ponderati a distanza inversa", comunemente denominati metodi Shepard. Eseguendo ognuno degli otto punti da eq (6) tramite l'algoritmo, vengono ottenuti otto punti di controllo, ognuno con *I,**G,**B* e *L*,*un* valore ,*b,* che vengono inseriti nel pool con i dati di esempio originali.

Per garantire che il modello produca sempre valori di colore validi e per l'integrità e la stabilità del sistema nell'intera pipeline di elaborazione dei colori, è necessario eseguire un ritaglio finale nell'output del modello polinomiale. La gamut visiva CIE è descritta dal componente acromatico (*Y* o *L* ) e dal componente cromatico (*xy* o *a'b',* che sono correlati allo spazio XYZ da una trasformazione proiettativa). Nell'implementazione corrente viene usata la cromaticità *a'b'* perché è direttamente correlata allo spazio CIELUV. Per qualsiasi *valore CIELAB,* ritagliare *prima L* in un valore non negativo:

![Mostra il ritaglio di L in un valore non negativo.](images/cdmp-formula31.png)

Per consentire l'estrapolazione per le evidenziazioni speculari, *L* non viene ritagliato a 100, il limite superiore "convenzionale" per *L* nello spazio lab.

Successivamente, se *L* = 0, *a* e *b* vengono ritagliati in modo che a =*b =* 0. Se *L* ? 0, calcola

![Visualizza la formula se L=0.](images/cdmp-formula32.png)

Questi sono i componenti di un vettore nel diagramma *a'b'* dal punto bianco (*u?'*,*v?'* ) al colore in questione. Definire il locus spettrale CIE come scafo convesso di tutti i punti (*a'*,*b'* ), parametrizzato dalla lunghezza d'onda ?:

![Mostra la formula per la lunghezza d'onda.](images/cdmp-formula33.png)

dove ![ Mostra le funzioni per la corrispondenza dei colori CIE.](images/cdmp-formula34.png) sono le funzioni di corrispondenza dei colori CIE per l'osservatore a 2 gradi. Se il vettore si trova all'esterno del locus CIE, il colore viene ritagliato fino al punto del locus CIE che rappresenta l'intersezione del locus e della linea definita dal vettore. Vedere Figura 5. Se si è verificato un ritaglio, il *valore a* *e b* viene ricostruito sottraendo prima *a?'* e *b?'* dall'oggetto *ritagliato a'* *e b'* e quindi moltiplicato per 13 *L.*

![Diagramma che mostra il grafico per l'algoritmo di ritaglio.](images/cdmp-lcd-dmp-figure5.png)

**Figura 5:** Algoritmo di ritaglio per i valori lab esterni alla gamma di oggetti visivi CIE

Nell'implementazione corrente, il locus spettrale CIE nel piano *a'b'* è rappresentato da una curva lineare a senso unico con 35 segmenti (corrispondente a una lunghezza d'onda compresa tra 360 nm e 700 nm inclusi). Ordinando i segmenti di linea in modo che gli angoli sottotendati in corrispondenza del punto bianco siano ascendente, che equivale a lunghezze d'onda decrescenti, il segmento di linea che si interseca con il raggio formato dal vettore precedente può essere trovato da una semplice ricerca binaria.

### <a name="rgb-printer-device-model-baseline"></a>Baseline del modello di dispositivo della stampante RGB

Una caratterizzazione del dispositivo di una stampante RGB consiste nella costruzione di un modello empirico del dispositivo che stima il colore CIELUV indipendente dal dispositivo per qualsiasi valore RGB specificato

Esistono due modi per costruire il modello empirico. Un modo è usare i dati del dispositivo per una stampante RGB e l'altro è usare i dati dei parametri analitici. Nella prima vengono usati i dati di misurazione forniti da un utente per un dispositivo stampante RGB per costruire una tabella di ricerca 3D (LUT). I dati di misurazione sono costituiti da valori XYZ per patch RGB campionate in modo uniforme. Le dimensioni di campionamento tipiche sono 9 o 17 per ogni componente. Ogni patch viene misurata con un colorimetro o uno spettrofotometro nello spazio CIEXYZ. Il valore XYZ per una patch viene quindi convertito in valore CIELUV, formando un LUT 3D. Nel modello di dispositivo, il metodo di interpolazione tetraedrale di Sakamoto viene applicato all'LUT 3D per stimare i dati CIELUV per un dato dato RGB. (Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[ 1 \] . I due brevetti menzionati sono scaduti. I dati dei parametri analitici passati nel secondo metodo sono semplicemente un LUT compilato in precedenza. In genere, tale LUT è stato compilato usando il primo metodo, anche se può essere compilato manualmente.

Nella gestione del colore corrente, il source map definito come mappa che passa dallo spazio RGB a uno spazio colore CIEXYZ indipendente dal dispositivo. La mappa di destinazione è definita come mappa che passa dallo spazio colore CIEXYZ indipendente dal dispositivo allo spazio RGB. È l'inverso del source map.

Il modello empirico viene usato direttamente nel source map. Esegue innanzitutto il mapping di dati RGB in dati CIELUV, che vengono convertiti in dati XYZ. Nella mappa di destinazione i dati CIEXYZ indipendenti dal dispositivo vengono prima convertiti in dati CIELUV. Quindi, il modello empirico e il metodo Newton-Raphson classico vengono usati per stimare i dati RGB migliori per i dati CIELUV. I dettagli sulla conversione da dati CieLUV a RGB sono i seguenti:

Dopo aver generato un LUT 3D da RGB a CieLUV, la mappa da RGB a LUV viene creata usando l'interpolazione tetraedrale su RGB. Questa mappa è denotata dalle equazioni seguenti:

![Mostra le equazioni per la mappa da R G B a L U V.](images/cdmp-image125.png)

L'inversione della mappa è costituita dalla risoluzione, per qualsiasi colore ![Mostra L U V.](images/cdmp-image127.png) , il sistema di equazioni non lineari seguente:

![Mostra le equazioni non lineari per lolving di qualsiasi colore L U V.](images/cdmp-image129.png)

Nella nuova CTE viene usata un'equazione non lineare basata sul metodo Newton-Raphson classico. Un'ipotesi iniziale, o *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) viene ottenuta eseguendo una ricerca in una "matrice di inizializzazione" costituita da una griglia uniforme 8x8x8 di coppie pre-calcolate (RGB, Luv). Viene scelto Luv corrispondente RGB più vicino all'L \* u \* \* v. Ogni punto nella matrice di valori di avviamento corrisponde al centro di una cella in modo che le iterazioni non inizino con un punto sulla faccia limite del cubo RGB. In altre parole, l'RGB dei semi è definito da: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At *the i* th step of Newton-Raphson, the next estimate Shows the ![ variables for the next estimate.](images/cdmp-image133.png) viene ottenuto dalla formula:

![Mostra la formula per la stima.](images/cdmp-image135.png)

L'iterazione viene arrestata quando l'errore (distanza nello spazio CIELUV) è minore di un livello di tolleranza pre-impostato (0,1 nella CTE) o quando il numero di iterazioni ha superato il numero massimo consentito di iterazioni (10 nella CTE). I valori per la tolleranza e il numero di iterazioni sono stati determinati empiricamente come effettivi. Nelle versioni future, il valore di tolleranza può essere modificato.

La matrice giacobina viene calcolata usando la differenza in avanti, ad eccezione di un punto limite (uno o più R, G, B è 1) in cui viene invece usata la differenza all'indietro. Invece di calcolare l'inverso della matrice giacobita, il sistema lineare viene risolto direttamente usando Gauss-Jordan'eliminazione con pivot completo.

Al termine delle iterazioni, la convergenza potrebbe ancora non essere ottenuta perché Newton-Raphson è un algoritmo "locale", vale a dire funziona bene solo se si inizia con un'ipotesi iniziale vicina alla soluzione vera. Se, alla fine delle iterazioni Newton-Raphson, la convergenza all'interno della tolleranza di errore predefinita non è stata raggiunta, le iterazioni vengono riavviate con un nuovo set di semi, definito come segue.

Ad esempio, la soluzione migliore ottenuta finora è (r, g, b). Da questa soluzione vengono derivati N semi posteriori, dove N = 4. Intuitivamente, la soluzione viene spostata "verso il centro" in una dimensione del passaggio che dipende da N. Vedere la figura 6.

![Diagramma che mostra le direzioni di perturbazione della soluzione.](images/cdmp-image136.png)

**Figura 6:** la direzione di perturbazione della soluzione dipende dall'ottetto in cui si trova.

In altre parole, se r 0,5, il valore sul canale R viene ridotto, in caso contrario il &gt; valore viene aumentato. Esiste una logica simile per i canali G e B. Le definizioni precise sono:

PERTURBAZIONE = 0,5/(N+1)

Dir(r) = -1 se r &gt; 0,5; +1 in caso contrario. Analogamente per Dir(g) e Dir(b)

The jth a posteriori seed, s ????, is (r + Dir(r) \* j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)

Provare la prima ???? e se offre una nuova soluzione entro la tolleranza di errore, è possibile arrestarsi. In caso contrario, provare la seconda ???? e così via fino all'Esima ????.

Gli schemi dell'intero algoritmo sono illustrati nella figura 7.

![Diagramma che mostra il flusso per l'inversione del modello di dispositivo.](images/cdmp-image138.png)

**Figura 7:** Schemi di inversione del modello di dispositivo

### <a name="rgb-virtual-device-model-baseline"></a>Baseline del modello di dispositivo virtuale RGB

Questo modello di dispositivo (DM) è un semplice algoritmo di riproduzione matrice/tono. La matrice è derivata dal punto bianco e dalle primarie usando algoritmi di scienza dei colori standard. La curva di riproduzione del tono deriva dai parametri di misurazione in base alle descrizioni ICC di CurveType e ParametricType (o invertita in base alle esigenze). I dettagli degli algoritmi interni verranno forniti dopo un'ulteriore convalida dei problemi di intervallo dinamico elevato.

Il modello di dispositivo virtuale RGB è una curva di riproduzione matrice/tono idealizzata, simile alla progettazione del profilo basato su matrice a tre componenti ICC. I parametri di "misurazione virtuale" del dm includono un valore punto bianco (CIEXYZ assoluto), valori primari RGB (CIEXYZ assoluti) e una curva di riproduzione del tono basata sui parametri ICC ParametricCurveType e CurveType nella formattazione XML coerente con gli schemi DMP.

La codifica del tipo di funzione ICC parametricCurveType e il supporto corrispondente in IRGBVirtualDeviceModelBase sono illustrati nella tabella seguente.



| Tipo di funzione                                         | Parametri                          | Tipo                                     | Nota                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Mostra la funzione 'GammaType'.](images/cdmp-image154.png)<br/> | g<br/>              | GammaType<br/>                 | Implementazione comune<br/>           |
| ![Mostra la funzione 'GammaOffsetGainType'.](images/cdmp-image156.png)<br/> | ga b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Mostra la funzione 'GammaOffsetGainOffsetType'.](images/cdmp-image158.png)<br/> | ga b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Mostra la funzione 'GammaOffsetGainGainType'.](images/cdmp-image160.png)<br/> | ga b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> (sRGB)<br/> |
| ![Mostra una funzione per i parametri 'g a b c d e f'.](images/cdmp-image162.png)<br/> | ga b c d e f<br/>   | N/A<br/>                       | Non supportato in WCS<br/>            |



 

La curva del tono per i dispositivi virtuali RGB viene applicata in DeviceToColorimetric tra i dati di input, pDeviceColors e la moltiplicazione della matrice. Per ColorimetricToDevice, è necessario usare un metodo per invertire la curva del tono. Nell'implementazione di base questa operazione viene eseguita tramite interpolazione diretta nella stessa curva tonale usata per DeviceToColorimetric.

Le curve devono essere specificate nei profili come coppie di numeri nello spazio mobile. Il primo numero rappresenta i valori in pDeviceColors. Il secondo numero rappresenta l'output della curva tonale. Tutti i valori nella curva del tono devono essere compresi tra minColorantUsed e maxColorantUsed. Le curve tono devono contenere almeno due voci: una per minColorantUsed e una per maxColorantUsed. Il numero massimo di voci in ToneCurve è 2048. In generale, più voci sono presenti nella tabella, più accuratamente è possibile modellare la curvatura. Tra le voci viene eseguita un'interpolazione lineare a pezzetti.

È possibile prendere in considerazione metodi di interpolazione alternativi. Se si conosce qualcosa sul comportamento sottostante del dispositivo, è possibile usare meno campioni e modellare in modo più accurato con una curva di ordine superiore. Ma se si usa il tipo di curva errato, si sarà molto imprecisi. Senza altre informazioni, non è possibile indovinare il tipo di curva. Usare quindi l'interpolazione lineare e fornire molti punti dati.

### <a name="cmyk-printer-device-model-baseline"></a>Baseline del modello di dispositivo della stampante CMYK

Una caratterizzazione del dispositivo di una stampante CMYK consiste nella costruzione di un modello empirico del dispositivo che stima il colore stampato per qualsiasi valore CMYK specificato. La caratterizzazione include anche l'inversione di questo modello in modo che sia possibile specificare una prescrizione del valore CMYK per un determinato colore da stampare. Questo valore è in genere definito in termini di valore CIEXYZ o CIELAB.

In genere, viene usata una destinazione IT8.7/3 contenente patch CMYK. Le patch sono costituite dal campionamento dello spazio CMYK in modo ben definito in modo da formare una griglia rettangolare (con spaziatura non uniforme in C, M, Y e K). Ogni patch viene quindi misurata con un colorimetro o uno spettrofotometro. Le misurazioni nei valori CIEXYZ formano quindi una tabella di ricerca (LUT), da cui viene creato un modello empirico della stampante usando il metodo di interpolazione di Sakamoto. US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[ 1 \] . I due brevetti menzionati sono scaduti.

Di seguito sono riportati i requisiti specifici per gli esempi di misurazione CMYK necessari per accettare un profilo del modello di dispositivo come valido dal modello di dispositivo di base della stampante CMYK. Il set di esempi è descritto più chiaramente come un set di cubi di esempio CMY, ognuno associato a un livello K specifico.

-   È necessario specificare almeno cubi CMY validi per i livelli K = 0 e K = 100.
-   I livelli K intermedi possono essere spaziati in modo non uniforme.
-   Qualsiasi livello K intermedio senza un cubo CMY valido verrà ignorato.
-   I cubi CMY possono usare intervalli di campionamento non uniformi (spaziatura della griglia), ma lo stesso set di intervalli di campionamento deve essere usato in tutte le dimensioni C, M e Y nel cubo CMY per un determinato livello K.
-   Ogni cubo CMY di livello K può usare un numero e una spaziatura diversi per gli intervalli di campionamento.
-   Tutti i cubi CMY devono contenere gli "angoli" del cubo CMY, ad esempio, campioni CMY \[ in corrispondenza di 0,0,0 \] , \[ 0,0,100 \] , \[ 0,100,0 \] , \[ 100,0,0 \] , \[ 0,100,100 \] , \[ 100,0,100 \] , \[ 100,100, 0 \] , \[ 100,100,100. \]
-   Tutti i livelli intermedi della griglia CMY devono essere campionati completamente in ogni canale. In altre parole, deve esistere un campione in corrispondenza di ogni intersezione di griglia 3D all'interno del cubo CMY.
-   Per i cubi K = 0 e K = 100 CMY, i cubi 2x2x2 "solo angoli" sono il minimo accettato come validi.

    \[NOTA: per i livelli K=0 e K=100, un cubo CMY 3x3x3 verrà elaborato come cubo "solo angoli" 2x2x2; il livello di campionamento intermedio viene ignorato. Nei cubi 4x4x4 e più grandi verranno usati tutti gli esempi su griglia.\]

-   Per i livelli K intermedi, i cubi CMY 4x4x4 sono il minimo accettato come validi.

Un profilo di alta qualità userà griglie di campionamento più fine del minimo necessario per la validità, in genere 9x9x9x9 o superiore. Gli esempi delle destinazioni IT8.7/3, IT8.7/4 ed ECI producono profili di modello di dispositivo (DMP) validi per il modello di dispositivo di base della stampante CMYK. Anche se questo modello di dispositivo è in grado di ignorare gli esempi estranei (fuori rete) in queste destinazioni, non è garantito che sia in grado di eseguire questa operazione per altre destinazioni, pertanto è consigliabile rimuovere campioni estranei dai set di misurazioni che vengono suddivisi nei profili per questo modello di dispositivo.

L'inversione del modello di stampante presenta maggiori difficoltà. Dato un colore di input in MODALITÀM, è necessario stabilire se questo colore rientra nella gamma della stampante. Esiste anche il problema relativo alla disposizione dei punti nello spazio dell'aspetto dei colori. Anche se è possibile disporre i valori CMYK in modo che cadano su una griglia rettangolare, come avviene nella destinazione IT8.7/3, non è possibile dire lo stesso dei colori stampati risultanti perché si trovano nello spazio dell'aspetto colore. In generale, sono sparsi nello spazio dell'aspetto dei colori senza un motivo particolare.

Esistono in genere due approcci al problema di inversione dei punti sparsi. Un approccio consiste nell'usare una suddivisione geometrica della gamma di stampanti usando solidi tridimensionali elementari, ad esempio tetrahedra. Una suddivisione della gamma delle stampanti nello spazio dell'aspetto dei colori può essere indotta dalla suddivisione corrispondente dello spazio CMY(K), vedere Hung \[ 93 \] , Kang \[ 97 \] . Questo approccio ha il vantaggio della semplicità di calcolo. Nel caso di un tetrahedron, in un'interpolazione vengono usati solo quattro punti. D'altra parte, il risultato dipende molto da alcuni punti, il che significa che un errore di misurazione avrà un effetto significativo sul risultato. Anche l'interpolazione tende a non essere uniforme. Il secondo approccio non presuppone alcuna suddivisione ed è basato sulla tecnica dell'interpolazione di dati sparsi. Un esempio classico è la tecnica di interpolazione di Shepard o metodo ponderato inverso (vedere Shepard \[ \] 68). In questo caso, vengono scelti diversi punti che circondano il punto di input, ognuno dei quali ha assegnato un peso, in genere in modo inversamente proporzionale alla distanza, e l'interpolante viene preso come media ponderata dei punti adiacenti. In questo approccio, la scelta dei punti adiacenti è fondamentale per le prestazioni. Anche se un numero troppo ridotto di punti può rendere non accurato e non uniforme l'interpolazione, troppi punti impongono un costo di calcolo elevato, poiché i pesi sono in genere funzioni non lineari e costose da calcolare.

I due approcci descritti in precedenza hanno entrambi problemi. L'approccio di suddivisione dipende in modo critico dai dati ragionevolmente vuoti dal rumore e in genere l'interpolazione non è molto uniforme. L'interpolazione di dati sparsi è più tollerante al rumore dei dati e in genere offre un interpolazione più uniforme, ma dal punto di vista del calcolo è più costosa.

La nuova CTE adotta un approccio alternativo. Il dispositivo CMYK viene considerato come una raccolta di diversi dispositivi CMY, ognuno dei quali ha un valore specifico di nero (K). Usando un algoritmo di selezione che accetta come parametri leggerezza e chroma, viene scelto un livello di nero. I valori CMY vengono ottenuti dall'inversione della tabella CMY in Luv corrispondente usando i metodi Newton utilizzati altrove dall'algoritmo di stampa RGB.

Seguire questa procedura.

1.  Stampare la destinazione di caratterizzazione, ovvero la destinazione IT8.7/3 o una destinazione contenente il campionamento dello spazio CMYK a intervalli regolari o irregolari.
2.  Misurare la destinazione usando uno spectrofotometro e convertire le misure nello spazio CIELUV.
3.  Costruire la mappa in avanti da CMYK a Luv.
4.  Usare la mappa in avanti per costruire un set di mappe DA CMY a Luv per un intervallo di valori K.
5.  Per qualsiasi valore Luv di input, il valore CMYK corrispondente viene ottenuto selezionando una delle mappe costruite nel passaggio 4 precedente e invertendo usando il metodo di Newton per ottenere un set di colori CMY associato al valore K selezionato.

I passaggi 1 e 2, che sono procedure standard, vengono eseguiti da un programma di profilatura che non fa parte della nuova CTE. La destinazione IT8.7/3 contiene un campionamento ragionevolmente dettagliato di tutti i valori CMYK a vari livelli di C, M, Y e K. In alternativa, è possibile usare una destinazione personalizzata con campionamento uniforme dei canali C, M, Y e K. Dopo aver stampato la destinazione, è possibile usare uno spectrofometro o un colorimetro per misurare il valore XYZ di ogni patch e il valore XYZ può essere convertito nel valore Luv usando il modello CIELUV.

Il passaggio 3, la costruzione della mappa in avanti da CMYK a Luv, può essere ottenuto applicando qualsiasi tecnica di interpolazione nota, ad esempio il metodo tetrahedral o multilineare, sulla griglia rettangolare nello spazio CMYK. Nella nuova CTE viene usata un'interpolazione tetraedrale a 4 dimensioni. Poiché le griglie di campionamento CMY sono in genere diverse per ogni livello di K, tuttavia, viene utilizzata una tecnica di super-campionamento, come descritto di seguito. Per un determinato punto CMYK, i livelli K di sandwiching vengono prima determinati in base al valore K. Introdurre quindi una "super-griglia" in ogni livello K che è un'unione delle griglie CMY in ognuno dei due livelli K. A ogni livello K, il valore Luv di qualsiasi punto della griglia appena introdotto viene ottenuto da un'interpolazione tetraedrale tridimensionale all'interno di tale livello K. Infine, in questa nuova griglia viene eseguita un'interpolazione tetraedrale 4-dimensionale per il punto CMYK specifico.

![Diagramma che illustra il supersampling.](images/cdmp-image163.png)

**Figura 8:** Supersampling

Il passaggio 4 costruisce un set di tabelle di ricerca DA CMY a Luv (LUT). La mappa in avanti costruita nel passaggio 3 viene chiamata ripetutamente per ricampionare lo spazio CMYK. Lo spazio colore CMYK viene campionato usando una spaziatura uniforme di K e un campionamento CMY diverso, ma ancora uniformemente disattato.

Il passaggio 5 è una procedura per ottenere il valore CMYK usando i LUT costruiti nel passaggio 4 per qualsiasi punto Luv di input. Il valore appropriato di K viene scelto analizzando la leggerezza e il grado di colore nel Luv richiesto. Dopo aver selezionato la tabella, i valori CMY vengono ottenuti dalla tabella usando il metodo di Newton ( come documentato in precedenza nel modello di dispositivo della stampante RGB).

Lo spazio CIELUV viene usato nel modello di stampante invece di CIEJab perché il modello di dispositivo deve essere basato esclusivamente sui dati colorimetrici disponibili nel DMP. Il DMP contiene dati colorimetrici per ogni patch misurata, incluso il punto bianco multimediale, quindi è possibile convertire i dati CIEXYZ in dati CIELUV. Tuttavia, non è possibile eseguire la conversione in UNAM02 JCh o Unto, perché non è possibile accedere alle informazioni sulle condizioni di visualizzazione nel DMP.

### <a name="rgb-projector-device-model-baseline"></a>Baseline del modello di dispositivo del proiettore RGB

Nota: molti proiettori RGB hanno più modalità operative. In una modalità, che è spesso l'impostazione predefinita e potrebbe essere chiamata "presentazione", la risposta del colore del proiettore è ottimizzata per la massima luminosità. In questa modalità, tuttavia, il proiettore perde la possibilità di riprodurre colori chiari e leggermente cromatici, ad esempio i gialli blu e alcuni toni di color chiaro. In un'altra modalità, spesso denominata "film", "video" o "sRGB", il proiettore è ottimizzato per la riproduzione di immagini realistiche e scene naturali. In questa modalità, la luminosità massima viene compromessa per migliorare la qualità complessiva della riproduzione del colore. Per ottenere una riproduzione soddisfacente del colore con i proiettori RGB, è necessario posizionare il proiettore in una modalità in cui sia possibile riprodurre una gamma uniforme di colori.

![Diagramma che mostra un modello di dispositivo D L P.](images/cdmp-image167.png)

**Figura 9:** Modello di dispositivo DLP

Un valore RGB in ingresso passa attraverso due percorsi di calcolo. Il primo è il modello a matrice, che determina un valore XYZ. Questa operazione è seguita immediatamente dalla conversione da XYZ a Luv. Il secondo è l'interpolazione LUT non uniforme che usa l'interpolazione tetrahedrale. L'output dell'interpolazione è già nello spazio Luv per costruzione. I due output vengono aggiunti per ottenere il valore Luv previsto. Viene infine convertito in XYZ, ovvero l'output previsto del modello colorimetrico per il dispositivo DLP.

Poiché i proiettori sono dispositivi di visualizzazione, supportano anche l'inversione del modello, ad esempio la trasformazione da XYZ a RGB. Poiché il modello di dispositivo trasforma lo spazio RGB nello spazio XYZ, che sono entrambi tridimensionali, l'inversione equivale a risolvere tre equazioni non lineari in tre incognite. Questa operazione può essere eseguita con tecniche standard di risoluzione delle equazioni, ad esempio Newton-Raphson. È tuttavia preferibile convertire prima XYZ in Luv e quindi invertire la trasformazione Luv in RGB, perché lo spazio Luv è più percettivamente lineare rispetto allo spazio XYZ.

### <a name="icc-device-model-baseline"></a>Baseline del modello di dispositivo ICC

L'interoperabilità del flusso di lavoro CITE ICC viene abilitata creando uno speciale profilo del modello di dispositivo di base del dispositivo ICC che archivia l'oggetto profilo e crea una trasformazione ICC usando un profilo XYZ no-op. Questa trasformazione viene quindi usata per la conversione tra i colori del dispositivo e CIEXYZ.

![Diagramma che illustra l'interoperabilità del flusso di lavoro C I T E I C.](images/cdmp-image168.png)

**Figura 10:** Interoperabilità del flusso di lavoro CITE ICC

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Windows Schemi e algoritmi del sistema di colori](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





