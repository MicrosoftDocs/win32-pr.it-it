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
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a><span data-ttu-id="efb4c-118">Schema e algoritmi del profilo del modello del dispositivo a colori WCS</span><span class="sxs-lookup"><span data-stu-id="efb4c-118">WCS Color Device Model Profile Schema and Algorithms</span></span>

<span data-ttu-id="efb4c-119">In questo argomento vengono fornite informazioni sullo schema del profilo del modello di dispositivo con colori WCS e sugli algoritmi associati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-119">This topic provides information about the WCS Color Device Model Profile Schema and its associated algorithms.</span></span>

<span data-ttu-id="efb4c-120">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="efb4c-120">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="efb4c-121">Overview</span><span class="sxs-lookup"><span data-stu-id="efb4c-121">Overview</span></span>](#overview)
-   [<span data-ttu-id="efb4c-122">Architettura del profilo del modello del dispositivo a colori</span><span class="sxs-lookup"><span data-stu-id="efb4c-122">Color Device Model Profile Architecture</span></span>](#color-device-model-profile-architecture)
-   [<span data-ttu-id="efb4c-123">Schema CDMP</span><span class="sxs-lookup"><span data-stu-id="efb4c-123">The CDMP Schema</span></span>](#the-cdmp-schema)
-   [<span data-ttu-id="efb4c-124">Aggiunta calibrazione CDMP v 2.0 WCS</span><span class="sxs-lookup"><span data-stu-id="efb4c-124">WCS CDMP v2.0 Calibration Addition</span></span>](#wcs-cdmp-v20-calibration-addition)
-   [<span data-ttu-id="efb4c-125">Elementi dello schema CDMP</span><span class="sxs-lookup"><span data-stu-id="efb4c-125">The CDMP Schema Elements</span></span>](#the-cdmp-schema-elements)
    -   [<span data-ttu-id="efb4c-126">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="efb4c-126">ColorDeviceModelProfile</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="efb4c-127">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="efb4c-127">ColorDeviceModel</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="efb4c-128">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="efb4c-128">NamespaceVersion</span></span>](#namespaceversion)
    -   [<span data-ttu-id="efb4c-129">Versione</span><span class="sxs-lookup"><span data-stu-id="efb4c-129">Version</span></span>](#namespaceversion)
    -   [<span data-ttu-id="efb4c-130">Documentazione</span><span class="sxs-lookup"><span data-stu-id="efb4c-130">Documentation</span></span>](#documentation)
    -   [<span data-ttu-id="efb4c-131">Elemento CRTDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-131">CRTDevice element</span></span>](#crtdevice-element)
    -   [<span data-ttu-id="efb4c-132">Elemento LCDDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-132">LCDDevice element</span></span>](#lcddevice-element)
    -   [<span data-ttu-id="efb4c-133">Elemento ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-133">ProjectorDevice element</span></span>](#projectordevice-element)
    -   [<span data-ttu-id="efb4c-134">Elemento ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-134">ScannerDevice element</span></span>](#scannerdevice-element)
    -   [<span data-ttu-id="efb4c-135">Elemento CameraDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-135">CameraDevice element</span></span>](#cameradevice-element)
    -   [<span data-ttu-id="efb4c-136">Elemento RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-136">RGBPrinterDevice element</span></span>](#rgbprinterdevice-element)
    -   [<span data-ttu-id="efb4c-137">Elemento CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-137">CMYKPrinterDevice element</span></span>](#cmykprinterdevice-element)
    -   [<span data-ttu-id="efb4c-138">Elemento RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-138">RGBVirtualDevice element</span></span>](#rgbvirtualdevice-element)
    -   [<span data-ttu-id="efb4c-139">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="efb4c-139">PlugInDeviceType</span></span>](#plugindevicetype)
    -   [<span data-ttu-id="efb4c-140">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-140">RGBVirtualMeasurementType</span></span>](#rgbvirtualmeasurementtype)
    -   [<span data-ttu-id="efb4c-141">GammaType</span><span class="sxs-lookup"><span data-stu-id="efb4c-141">GammaType</span></span>](#gammatype)
    -   [<span data-ttu-id="efb4c-142">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="efb4c-142">GammaOffsetGainType</span></span>](#gammaoffsetgaintype)
    -   [<span data-ttu-id="efb4c-143">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="efb4c-143">GammaOffsetGainLinearGainType</span></span>](#gammaoffsetgainlineargaintype)
    -   [<span data-ttu-id="efb4c-144">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="efb4c-144">ToneResponseCurvesType</span></span>](#toneresponsecurvestype)
    -   [<span data-ttu-id="efb4c-145">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="efb4c-145">GamutBoundarySamplesType</span></span>](#gamutboundarysamplestype)
    -   [<span data-ttu-id="efb4c-146">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="efb4c-146">FloatPairList</span></span>](#floatpairlist)
    -   [<span data-ttu-id="efb4c-147">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-147">CMYKPrinterMeasurementType</span></span>](#cmykprintermeasurementtype)
    -   [<span data-ttu-id="efb4c-148">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-148">RGBPrinterMeasurementType</span></span>](#rgbprintermeasurementtype)
    -   [<span data-ttu-id="efb4c-149">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-149">RGBCaptureMeasurementType</span></span>](#rgbcapturemeasurementtype)
    -   [<span data-ttu-id="efb4c-150">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="efb4c-150">OneBasedIndex</span></span>](#onebasedindex)
    -   [<span data-ttu-id="efb4c-151">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-151">RGBProjectorMeasurementType</span></span>](#rgbprojectormeasurementtype)
    -   [<span data-ttu-id="efb4c-152">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-152">DisplayMeasurementType</span></span>](#displaymeasurementtype)
    -   [<span data-ttu-id="efb4c-153">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="efb4c-153">MeasurementConditionsType</span></span>](#measurementconditionstype)
    -   [<span data-ttu-id="efb4c-154">GeometryType</span><span class="sxs-lookup"><span data-stu-id="efb4c-154">GeometryType</span></span>](#geometrytype)
    -   [<span data-ttu-id="efb4c-155">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="efb4c-155">RGBPrimariesGroup</span></span>](#rgbprimariesgroup)
    -   [<span data-ttu-id="efb4c-156">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="efb4c-156">NonNegativeCMYKSampleType</span></span>](#nonnegativecmyksampletype)
    -   [<span data-ttu-id="efb4c-157">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="efb4c-157">NonNegativeRGBSampleType</span></span>](#nonnegativergbsampletype)
    -   [<span data-ttu-id="efb4c-158">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="efb4c-158">NonNegativeCMYKType</span></span>](#nonnegativecmyktype)
    -   [<span data-ttu-id="efb4c-159">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="efb4c-159">NonNegativeRGBType</span></span>](#nonnegativergbtype)
    -   [<span data-ttu-id="efb4c-160">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="efb4c-160">ExtensionType</span></span>](#extensiontype)
    -   [<span data-ttu-id="efb4c-161">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-161">NonNegativeXYZType</span></span>](#nonnegativexyztype)
    -   [<span data-ttu-id="efb4c-162">XYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-162">XYZType</span></span>](#nonnegativexyztype)
-   [<span data-ttu-id="efb4c-163">Algoritmi di base di CDMP</span><span class="sxs-lookup"><span data-stu-id="efb4c-163">The CDMP Baseline Algorithms</span></span>](#the-cdmp-baseline-algorithms)
    -   [<span data-ttu-id="efb4c-164">Baseline modello di dispositivo CRT</span><span class="sxs-lookup"><span data-stu-id="efb4c-164">CRT Device Model Baseline</span></span>](#crt-device-model-baseline)
    -   [<span data-ttu-id="efb4c-165">Linea di base del modello di dispositivo LCD</span><span class="sxs-lookup"><span data-stu-id="efb4c-165">LCD Device Model Baseline</span></span>](#lcd-device-model-baseline)
    -   [<span data-ttu-id="efb4c-166">Baseline modello dispositivo stampante RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-166">RGB Printer Device Model Baseline</span></span>](#rgb-printer-device-model-baseline)
    -   [<span data-ttu-id="efb4c-167">Linea di base del modello di dispositivo virtuale RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-167">RGB Virtual Device Model Baseline</span></span>](#rgb-virtual-device-model-baseline)
    -   [<span data-ttu-id="efb4c-168">Baseline modello di dispositivo stampante CMYK</span><span class="sxs-lookup"><span data-stu-id="efb4c-168">CMYK Printer Device Model Baseline</span></span>](#cmyk-printer-device-model-baseline)
    -   [<span data-ttu-id="efb4c-169">Baseline modello di dispositivo proiettore RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-169">RGB Projector Device Model Baseline</span></span>](#rgb-projector-device-model-baseline)
    -   [<span data-ttu-id="efb4c-170">Baseline del modello di dispositivo ICC</span><span class="sxs-lookup"><span data-stu-id="efb4c-170">ICC Device Model Baseline</span></span>](#icc-device-model-baseline)
-   [<span data-ttu-id="efb4c-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efb4c-171">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="efb4c-172">Panoramica</span><span class="sxs-lookup"><span data-stu-id="efb4c-172">Overview</span></span>

<span data-ttu-id="efb4c-173">Questo schema viene utilizzato per specificare il contenuto di un profilo del modello del dispositivo a colori (CDMP).</span><span class="sxs-lookup"><span data-stu-id="efb4c-173">This schema is used to specify the content of a color device model profile(CDMP).</span></span> <span data-ttu-id="efb4c-174">Gli algoritmi di base associati sono descritti di seguito.</span><span class="sxs-lookup"><span data-stu-id="efb4c-174">The associated baseline algorithms are described below.</span></span>

<span data-ttu-id="efb4c-175">Lo schema DMP (Basic Device Model Profile) è costituito dai dati di misurazione del campionamento.</span><span class="sxs-lookup"><span data-stu-id="efb4c-175">The basic device model profile (DMP) schema consists of the sampling measurement data.</span></span>

<span data-ttu-id="efb4c-176">Il componente di campionamento del XML Schema DMP fornisce supporto per gli obiettivi di misurazione dei colori di base, concentrandosi su destinazioni e destinazioni standard più comuni ottimizzate per i modelli di dispositivo di base.</span><span class="sxs-lookup"><span data-stu-id="efb4c-176">The sampling component of the DMP XML schema provides support for basic color measurement targets, focusing on common standard targets and targets optimized for the baseline device models.</span></span>

<span data-ttu-id="efb4c-177">Il profilo del dispositivo fornisce inoltre informazioni specifiche sul modello di dispositivo di destinazione e fornisce un criterio che il modello di dispositivo di fallback di base può utilizzare se il modello di destinazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="efb4c-177">In addition, the device profile provides specific information on the targeted device model and provides a policy that the baseline fallback device model can use if the targeted model is unavailable.</span></span> <span data-ttu-id="efb4c-178">Le istanze del profilo possono includere estensioni private mediante meccanismi di estensione XML standard.</span><span class="sxs-lookup"><span data-stu-id="efb4c-178">The profile instances can include private extensions using standard XML extension mechanisms.</span></span>

## <a name="color-device-model-profile-architecture"></a><span data-ttu-id="efb4c-179">Architettura del profilo del modello del dispositivo a colori</span><span class="sxs-lookup"><span data-stu-id="efb4c-179">Color Device Model Profile Architecture</span></span>

![Diagramma che mostra le informazioni che costituiscono un profilo del modello di dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a><span data-ttu-id="efb4c-181">Schema CDMP</span><span class="sxs-lookup"><span data-stu-id="efb4c-181">The CDMP Schema</span></span>


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



## <a name="wcs-cdmp-v20-calibration-addition"></a><span data-ttu-id="efb4c-182">Aggiunta calibrazione CDMP v 2.0 WCS</span><span class="sxs-lookup"><span data-stu-id="efb4c-182">WCS CDMP v2.0 Calibration Addition</span></span>

<span data-ttu-id="efb4c-183">L'elemento **ColorDeviceModel** dello schema CDMP è stato aggiornato in Windows 7 in modo da includere il nuovo elemento Calibration.</span><span class="sxs-lookup"><span data-stu-id="efb4c-183">The **ColorDeviceModel** element of the CDMP schema has been updated in Windows 7 to include the new calibration element.</span></span> <span data-ttu-id="efb4c-184">Di seguito viene illustrata la modifica allo schema CDMP.</span><span class="sxs-lookup"><span data-stu-id="efb4c-184">The following shows the change to the CDMP schema.</span></span>


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



## <a name="the-cdmp-schema-elements"></a><span data-ttu-id="efb4c-185">Elementi dello schema CDMP</span><span class="sxs-lookup"><span data-stu-id="efb4c-185">The CDMP Schema Elements</span></span>

> [!Note]  
> <span data-ttu-id="efb4c-186">Le primarie sono esempi primari di rosso, verde, blu, nero e bianco.</span><span class="sxs-lookup"><span data-stu-id="efb4c-186">Primaries are primary samples of red, green, blue, black, and white.</span></span> <span data-ttu-id="efb4c-187">Una rampa primaria è una rampa tonale da minima luminanza a un valore primario completo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-187">A primary ramp is a tonal ramp from least luminance to full primary value.</span></span> <span data-ttu-id="efb4c-188">Il numero massimo di voci in una rampa di tono è 4096.</span><span class="sxs-lookup"><span data-stu-id="efb4c-188">The maximum number of entries in a tone ramp is 4096.</span></span>

 

> [!Note]  
> <span data-ttu-id="efb4c-189">Per i dati di misurazione è necessario DMPs.</span><span class="sxs-lookup"><span data-stu-id="efb4c-189">DMPs are required to have measurement data.</span></span>

 

### <a name="colordevicemodelprofile"></a><span data-ttu-id="efb4c-190">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="efb4c-190">ColorDeviceModelProfile</span></span>

<span data-ttu-id="efb4c-191">Questo elemento è di tipo ColorDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="efb4c-191">This element is of type ColorDeviceModel.</span></span>

<span data-ttu-id="efb4c-192">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-192">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="colordevicemodel"></a><span data-ttu-id="efb4c-193">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="efb4c-193">ColorDeviceModel</span></span>

<span data-ttu-id="efb4c-194">Questo elemento è una sequenza dei sottoelementi seguenti</span><span class="sxs-lookup"><span data-stu-id="efb4c-194">This element is a sequence of the following sub-elements</span></span>

1.  <span data-ttu-id="efb4c-195">Stringa ProfileName,</span><span class="sxs-lookup"><span data-stu-id="efb4c-195">ProfileName string,</span></span>
2.  <span data-ttu-id="efb4c-196">stringa di descrizione facoltativa,</span><span class="sxs-lookup"><span data-stu-id="efb4c-196">optional Description string,</span></span>
3.  <span data-ttu-id="efb4c-197">stringa autore facoltativa,</span><span class="sxs-lookup"><span data-stu-id="efb4c-197">optional Author string,</span></span>
4.  <span data-ttu-id="efb4c-198">facoltativo MeasurementConditions MeasurementConditionsType,</span><span class="sxs-lookup"><span data-stu-id="efb4c-198">optional MeasurementConditions MeasurementConditionsType,</span></span>
5.  <span data-ttu-id="efb4c-199">Self-Luminous valore booleano,</span><span class="sxs-lookup"><span data-stu-id="efb4c-199">Self-Luminous Boolean,</span></span>
6.  <span data-ttu-id="efb4c-200">MaxColorant float,</span><span class="sxs-lookup"><span data-stu-id="efb4c-200">MaxColorant float,</span></span>
7.  <span data-ttu-id="efb4c-201">MinColorant float,</span><span class="sxs-lookup"><span data-stu-id="efb4c-201">MinColorant float,</span></span>
8.  <span data-ttu-id="efb4c-202">Scelta di elementi</span><span class="sxs-lookup"><span data-stu-id="efb4c-202">Choice of elements</span></span>
    1.  <span data-ttu-id="efb4c-203">CRTDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-203">CRTDevice,</span></span>
    2.  <span data-ttu-id="efb4c-204">LCDDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-204">LCDDevice,</span></span>
    3.  <span data-ttu-id="efb4c-205">RGBProjectorDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-205">RGBProjectorDevice,</span></span>
    4.  <span data-ttu-id="efb4c-206">ScannerDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-206">ScannerDevice,</span></span>
    5.  <span data-ttu-id="efb4c-207">CameraDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-207">CameraDevice,</span></span>
    6.  <span data-ttu-id="efb4c-208">RGBPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-208">RGBPrinterDevice,</span></span>
    7.  <span data-ttu-id="efb4c-209">CMYKPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-209">CMYKPrinterDevice,</span></span>
    8.  <span data-ttu-id="efb4c-210">RGBVirtualDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-210">RGBVirtualDevice,</span></span>
9.  <span data-ttu-id="efb4c-211">PlugInDevice,</span><span class="sxs-lookup"><span data-stu-id="efb4c-211">PlugInDevice,</span></span>
10. <span data-ttu-id="efb4c-212">Estensione facoltativa ExtensionType</span><span class="sxs-lookup"><span data-stu-id="efb4c-212">optional Extension ExtensionType</span></span>

<span data-ttu-id="efb4c-213">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-213">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="efb4c-214">Gli elementi secondari stringa hanno un massimo di 10.000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="efb4c-214">String sub-elements have a maximum of 10,000 characters.</span></span> <span data-ttu-id="efb4c-215">Il sottoelemento MaxColorant deve essere maggiore o uguale a zero (0) e maggiore del sottoelemento MinColorant.</span><span class="sxs-lookup"><span data-stu-id="efb4c-215">The MaxColorant sub-element must be greater than or equal to zero (0) and greater than the MinColorant sub-element.</span></span> <span data-ttu-id="efb4c-216">Il valore di MinColorant può essere negativo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-216">The MinColorant can be negative.</span></span>

### <a name="namespaceversion"></a><span data-ttu-id="efb4c-217">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="efb4c-217">NamespaceVersion</span></span>

<span data-ttu-id="efb4c-218">xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="efb4c-218">xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

<span data-ttu-id="efb4c-219">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="efb4c-219">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

### <a name="version"></a><span data-ttu-id="efb4c-220">Versione</span><span class="sxs-lookup"><span data-stu-id="efb4c-220">Version</span></span>

<span data-ttu-id="efb4c-221">Version = "1,0" con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="efb4c-221">Version = "1.0" with Windows Vista.</span></span>

<span data-ttu-id="efb4c-222">**Condizioni di convalida:** Qualsiasi valore di versione &gt; 0,1 o &lt; = 2,0 è valido per supportare le modifiche non di rilievo nel formato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-222">**Validation conditions:** Any version value &gt;0.1 or &lt;=2.0 is valid to support non-breaking changes to the format.</span></span>

### <a name="documentation"></a><span data-ttu-id="efb4c-223">Documentazione</span><span class="sxs-lookup"><span data-stu-id="efb4c-223">Documentation</span></span>

<span data-ttu-id="efb4c-224">Schema del profilo del modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-224">Device Model Profile schema.</span></span>

<span data-ttu-id="efb4c-225">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efb4c-225">Copyright (C) Microsoft.</span></span> <span data-ttu-id="efb4c-226">Tutti i diritti sono riservati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-226">All rights reserved.</span></span>

### <a name="crtdevice-element"></a><span data-ttu-id="efb4c-227">Elemento CRTDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-227">CRTDevice element</span></span>

<span data-ttu-id="efb4c-228">Questo elemento è una sequenza di sottoelementi di un DisplayMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="efb4c-228">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="efb4c-229">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-229">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="lcddevice-element"></a><span data-ttu-id="efb4c-230">Elemento LCDDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-230">LCDDevice element</span></span>

<span data-ttu-id="efb4c-231">Questo elemento è una sequenza di sottoelementi di un DisplayMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="efb4c-231">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="efb4c-232">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-232">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="projectordevice-element"></a><span data-ttu-id="efb4c-233">Elemento ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-233">ProjectorDevice element</span></span>

<span data-ttu-id="efb4c-234">Questo elemento è una sequenza di sottoelementi di un RGBProjectorMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="efb4c-234">This element is a sequence of sub-elements of a MeasurementData RGBProjectorMeasurementType.</span></span>

<span data-ttu-id="efb4c-235">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-235">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="scannerdevice-element"></a><span data-ttu-id="efb4c-236">Elemento ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-236">ScannerDevice element</span></span>

<span data-ttu-id="efb4c-237">Questo elemento è una sequenza di sottoelementi di un RGBCaptureMeasurementType MeasurementData</span><span class="sxs-lookup"><span data-stu-id="efb4c-237">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="efb4c-238">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-238">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cameradevice-element"></a><span data-ttu-id="efb4c-239">Elemento CameraDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-239">CameraDevice element</span></span>

<span data-ttu-id="efb4c-240">Questo elemento è una sequenza di sottoelementi di un RGBCaptureMeasurementType MeasurementData</span><span class="sxs-lookup"><span data-stu-id="efb4c-240">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="efb4c-241">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-241">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbprinterdevice-element"></a><span data-ttu-id="efb4c-242">Elemento RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-242">RGBPrinterDevice element</span></span>

<span data-ttu-id="efb4c-243">Questo elemento è una sequenza di sottoelementi di un RGBPrinterMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="efb4c-243">This element is a sequence of sub-elements of a MeasurementData RGBPrinterMeasurementType.</span></span>

<span data-ttu-id="efb4c-244">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-244">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cmykprinterdevice-element"></a><span data-ttu-id="efb4c-245">Elemento CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-245">CMYKPrinterDevice element</span></span>

<span data-ttu-id="efb4c-246">Questo elemento è una sequenza di sottoelementi di un CMYKPrinterMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="efb4c-246">This element is a sequence of sub-elements of a MeasurementData CMYKPrinterMeasurementType.</span></span>

<span data-ttu-id="efb4c-247">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-247">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbvirtualdevice-element"></a><span data-ttu-id="efb4c-248">Elemento RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="efb4c-248">RGBVirtualDevice element</span></span>

<span data-ttu-id="efb4c-249">Questo elemento è una sequenza di sottoelementi di un RGBVirtualMeasurementDataType.</span><span class="sxs-lookup"><span data-stu-id="efb4c-249">This element is a sequence of sub-elements of a RGBVirtualMeasurementDataType.</span></span>

<span data-ttu-id="efb4c-250">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-250">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="plugindevicetype"></a><span data-ttu-id="efb4c-251">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="efb4c-251">PlugInDeviceType</span></span>

<span data-ttu-id="efb4c-252">Questo elemento è una sequenza di un GUID GUIDType e di tutti gli elementi secondari.</span><span class="sxs-lookup"><span data-stu-id="efb4c-252">This element is a sequence of a GUID GUIDType and any sub-elements.</span></span>

<span data-ttu-id="efb4c-253">**Condizioni di convalida:** Il GUID viene usato per trovare la corrispondenza con il GUID della dll del plug-in DM.</span><span class="sxs-lookup"><span data-stu-id="efb4c-253">**Validation conditions:** The GUID is used to match the DM PlugIn Dll GUID.</span></span> <span data-ttu-id="efb4c-254">Sono presenti un massimo di 100.000 sottoelementi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-254">There are a maximum of 100,000 custom sub-elements.</span></span>

### <a name="rgbvirtualmeasurementtype"></a><span data-ttu-id="efb4c-255">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-255">RGBVirtualMeasurementType</span></span>

<span data-ttu-id="efb4c-256">Questo elemento è una sequenza composta da</span><span class="sxs-lookup"><span data-stu-id="efb4c-256">This element is a sequence consisting of</span></span>

1.  <span data-ttu-id="efb4c-257">Gruppo RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="efb4c-257">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="efb4c-258">Scelta di</span><span class="sxs-lookup"><span data-stu-id="efb4c-258">A choice of</span></span>
3.  -   <span data-ttu-id="efb4c-259">Gamma</span><span class="sxs-lookup"><span data-stu-id="efb4c-259">Gamma</span></span>
    -   <span data-ttu-id="efb4c-260">GammaOffsetGain</span><span class="sxs-lookup"><span data-stu-id="efb4c-260">GammaOffsetGain</span></span>
    -   <span data-ttu-id="efb4c-261">GammaOffsetGainLinearGam</span><span class="sxs-lookup"><span data-stu-id="efb4c-261">GammaOffsetGainLinearGam</span></span>
    -   <span data-ttu-id="efb4c-262">Elementi ToneResponseCurves</span><span class="sxs-lookup"><span data-stu-id="efb4c-262">ToneResponseCurves elements</span></span>

4.  <span data-ttu-id="efb4c-263">GamutBoundarySamplesType GamutBoundarySamples facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-263">optional GamutBoundarySamples GamutBoundarySamplesType</span></span>
5.  <span data-ttu-id="efb4c-264">DateTime TimeStamp</span><span class="sxs-lookup"><span data-stu-id="efb4c-264">TimeStamp dateTime</span></span>

<span data-ttu-id="efb4c-265">**Condizioni di convalida:** Ogni sottoelemento di questi tipi presenta le proprie condizioni di convalida.</span><span class="sxs-lookup"><span data-stu-id="efb4c-265">**Validation conditions:** Each sub-element of these types has its own validation conditions.</span></span>

### <a name="gammatype"></a><span data-ttu-id="efb4c-266">GammaType</span><span class="sxs-lookup"><span data-stu-id="efb4c-266">GammaType</span></span>

<span data-ttu-id="efb4c-267">Questo elemento è un tipo complesso costituito dall'attributo</span><span class="sxs-lookup"><span data-stu-id="efb4c-267">This element is a complex type consisting of the attribute</span></span>

-   <span data-ttu-id="efb4c-268">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="efb4c-268">Gamma NonNegativeFloatType</span></span>

<span data-ttu-id="efb4c-269">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-269">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgaintype"></a><span data-ttu-id="efb4c-270">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="efb4c-270">GammaOffsetGainType</span></span>

<span data-ttu-id="efb4c-271">Questo elemento è un tipo complesso costituito dagli attributi</span><span class="sxs-lookup"><span data-stu-id="efb4c-271">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="efb4c-272">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="efb4c-272">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="efb4c-273">Offset NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="efb4c-273">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="efb4c-274">Ottieni NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="efb4c-274">Gain NonNegativeFloatType</span></span>

<span data-ttu-id="efb4c-275">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-275">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgainlineargaintype"></a><span data-ttu-id="efb4c-276">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="efb4c-276">GammaOffsetGainLinearGainType</span></span>

<span data-ttu-id="efb4c-277">Questo elemento è un tipo complesso costituito dagli attributi</span><span class="sxs-lookup"><span data-stu-id="efb4c-277">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="efb4c-278">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="efb4c-278">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="efb4c-279">Offset NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="efb4c-279">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="efb4c-280">Ottieni NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="efb4c-280">Gain NonNegativeFloatType</span></span>
-   <span data-ttu-id="efb4c-281">LinearGain NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="efb4c-281">LinearGain NonNegativeFloatType</span></span>
-   <span data-ttu-id="efb4c-282">TransitionPoint NonNegativeFloatType.</span><span class="sxs-lookup"><span data-stu-id="efb4c-282">TransitionPoint NonNegativeFloatType.</span></span>

<span data-ttu-id="efb4c-283">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-283">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="toneresponsecurvestype"></a><span data-ttu-id="efb4c-284">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="efb4c-284">ToneResponseCurvesType</span></span>

<span data-ttu-id="efb4c-285">Questo elemento è una sequenza di</span><span class="sxs-lookup"><span data-stu-id="efb4c-285">This element is a sequence of</span></span>

1.  <span data-ttu-id="efb4c-286">RedTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="efb4c-286">RedTRC FloatPairList</span></span>
2.  <span data-ttu-id="efb4c-287">GreenTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="efb4c-287">GreenTRC FloatPairList</span></span>
3.  <span data-ttu-id="efb4c-288">BlueTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="efb4c-288">BlueTRC FloatPairList</span></span>

<span data-ttu-id="efb4c-289">L'elemento dispone anche di un attributo TRCLength di tipo unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="efb4c-289">The element also has an attribute TRCLength of unsignedint type.</span></span>

<span data-ttu-id="efb4c-290">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-290">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gamutboundarysamplestype"></a><span data-ttu-id="efb4c-291">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="efb4c-291">GamutBoundarySamplesType</span></span>

<span data-ttu-id="efb4c-292">Questo elemento è una sequenza di RGBTypes RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-292">This element is a sequence of RGB RGBTypes.</span></span>

<span data-ttu-id="efb4c-293">**Condizioni di convalida:** Numero massimo di occorrenze attualmente non vincolate, da raggiungere in base ai commenti del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-293">**Validation conditions:** Currently unbounded maximum occurences, to be capped based on industry feedback.</span></span>

### <a name="floatpairlist"></a><span data-ttu-id="efb4c-294">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="efb4c-294">FloatPairList</span></span>

<span data-ttu-id="efb4c-295">Questo elemento è un tipo semplice di elenco di coppie di float.</span><span class="sxs-lookup"><span data-stu-id="efb4c-295">This element is a simple type of list of pairs of floats.</span></span>

<span data-ttu-id="efb4c-296">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-296">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="cmykprintermeasurementtype"></a><span data-ttu-id="efb4c-297">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-297">CMYKPrinterMeasurementType</span></span>

<span data-ttu-id="efb4c-298">Questo elemento è un</span><span class="sxs-lookup"><span data-stu-id="efb4c-298">This element is a</span></span>

1. <span data-ttu-id="efb4c-299">sequenza dell'elemento cubocolori costituito da una sequenza di NonNegativeCMYKSampleType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-299">sequence of ColorCube element consisting of a sequence of Sample NonNegativeCMYKSampleType</span></span>

2. <span data-ttu-id="efb4c-300">TimeStamp dateTime (attributo).</span><span class="sxs-lookup"><span data-stu-id="efb4c-300">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="efb4c-301">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-301">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprintermeasurementtype"></a><span data-ttu-id="efb4c-302">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-302">RGBPrinterMeasurementType</span></span>

<span data-ttu-id="efb4c-303">Questo elemento è un</span><span class="sxs-lookup"><span data-stu-id="efb4c-303">This element is a</span></span>

1. <span data-ttu-id="efb4c-304">sequenza dell'elemento cubocolori costituito da una sequenza di NonNegativeRGBSampleType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-304">sequence of ColorCube element consisting of a sequence of Sample NonNegativeRGBSampleType</span></span>

2. <span data-ttu-id="efb4c-305">TimeStamp dateTime (attributo).</span><span class="sxs-lookup"><span data-stu-id="efb4c-305">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="efb4c-306">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-306">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbcapturemeasurementtype"></a><span data-ttu-id="efb4c-307">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-307">RGBCaptureMeasurementType</span></span>

<span data-ttu-id="efb4c-308">Questo elemento è una sequenza di</span><span class="sxs-lookup"><span data-stu-id="efb4c-308">This element is a sequence of</span></span>

1.  <span data-ttu-id="efb4c-309">ComplexType PrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="efb4c-309">PrimaryIndex complexType of</span></span>
2.  1.  <span data-ttu-id="efb4c-310">OneBasedIndex bianco</span><span class="sxs-lookup"><span data-stu-id="efb4c-310">White OneBasedIndex</span></span>
    2.  <span data-ttu-id="efb4c-311">OneBasedIndex nero facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-311">Optional Black OneBasedIndex</span></span>
    3.  <span data-ttu-id="efb4c-312">OneBasedIndex rosso facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-312">Optional Red OneBasedIndex</span></span>
    4.  <span data-ttu-id="efb4c-313">OneBasedIndex verde facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-313">Optional Green OneBasedIndex</span></span>
    5.  <span data-ttu-id="efb4c-314">OneBasedIndex blu facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-314">Optional Blue OneBasedIndex</span></span>
    6.  <span data-ttu-id="efb4c-315">OneBasedIndex ciano facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-315">Optional Cyan OneBasedIndex</span></span>
    7.  <span data-ttu-id="efb4c-316">OneBasedIndex magenta facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-316">Optional Magenta OneBasedIndex</span></span>
    8.  <span data-ttu-id="efb4c-317">OneBasedIndex giallo facoltativo</span><span class="sxs-lookup"><span data-stu-id="efb4c-317">Optional Yellow OneBasedIndex</span></span>

3.  <span data-ttu-id="efb4c-318">NeutralIndices delle righe di OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="efb4c-318">NeutralIndices of lines of OneBasedIndex</span></span>
4.  <span data-ttu-id="efb4c-319">Sequenza ColorSamples di NonNegativeRGBSampleType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-319">ColorSamples sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="efb4c-320">L'elemento include anche un attributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="efb4c-320">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="efb4c-321">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-321">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="onebasedindex"></a><span data-ttu-id="efb4c-322">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="efb4c-322">OneBasedIndex</span></span>

<span data-ttu-id="efb4c-323">Questo elemento è un tipo semplice di base di limitazione senza segno int con valore minInclusive = "1".</span><span class="sxs-lookup"><span data-stu-id="efb4c-323">This element is a simple type of restriction base unsigned int with minInclusive value = "1."</span></span>

<span data-ttu-id="efb4c-324">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-324">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprojectormeasurementtype"></a><span data-ttu-id="efb4c-325">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-325">RGBProjectorMeasurementType</span></span>

<span data-ttu-id="efb4c-326">Questo elemento è una sequenza di</span><span class="sxs-lookup"><span data-stu-id="efb4c-326">This element is a sequence of</span></span>

1.  <span data-ttu-id="efb4c-327">Gruppo RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="efb4c-327">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="efb4c-328">elemento ColorSamples costituito dalla sequenza di NonNegativeRGBSampleType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-328">element ColorSamples consisting of sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="efb4c-329">L'elemento include anche un attributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="efb4c-329">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="efb4c-330">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-330">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="displaymeasurementtype"></a><span data-ttu-id="efb4c-331">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="efb4c-331">DisplayMeasurementType</span></span>

<span data-ttu-id="efb4c-332">Questo elemento è una sequenza di</span><span class="sxs-lookup"><span data-stu-id="efb4c-332">This element is a sequence of</span></span>

1.  <span data-ttu-id="efb4c-333">RGBPrimariesGroup gruppo</span><span class="sxs-lookup"><span data-stu-id="efb4c-333">group RGBPrimariesGroup</span></span>
2.  <span data-ttu-id="efb4c-334">GrayRamp della sequenza di NonNegativeRGBType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-334">GrayRamp of sequence of Sample NonNegativeRGBType</span></span>
3.  <span data-ttu-id="efb4c-335">RedRamp della sequenza di NonNegativeRGBType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-335">RedRamp of sequence of Sample NonNegativeRGBType</span></span>
4.  <span data-ttu-id="efb4c-336">GreenRamp della sequenza di NonNegativeRGBType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-336">GreenRamp of sequence of Sample NonNegativeRGBType</span></span>
5.  <span data-ttu-id="efb4c-337">BlueRamp della sequenza di NonNegativeRGBType di esempio</span><span class="sxs-lookup"><span data-stu-id="efb4c-337">BlueRamp of sequence of Sample NonNegativeRGBType</span></span>

<span data-ttu-id="efb4c-338">L'elemento DisplayMeasurementType include anche un attributo TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="efb4c-338">The DisplayMeasurementType element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="efb4c-339">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-339">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="measurementconditionstype"></a><span data-ttu-id="efb4c-340">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="efb4c-340">MeasurementConditionsType</span></span>

<span data-ttu-id="efb4c-341">MeasurementConditionsType è una sequenza di sottoelementi che contiene:</span><span class="sxs-lookup"><span data-stu-id="efb4c-341">The MeasurementConditionsType is a sequence of sub-elements that contains:</span></span>

1.  <span data-ttu-id="efb4c-342">Valore di enumerazione di stringhe con limitazione dello spazio dei colore di "CIE XYZ"</span><span class="sxs-lookup"><span data-stu-id="efb4c-342">ColorSpace restricted string enumeration value of "CIEXYZ"</span></span>
2.  <span data-ttu-id="efb4c-343">scelta facoltativa dell'enumerazione WhitePoint NonNegativeXYZType o WhitePointName String dei valori D50, D65, A o F2</span><span class="sxs-lookup"><span data-stu-id="efb4c-343">optional choice of WhitePoint NonNegativeXYZType or WhitePointName string enumeration of values D50, D65, A, or F2</span></span>
3.  <span data-ttu-id="efb4c-344">Geometria GeometryType</span><span class="sxs-lookup"><span data-stu-id="efb4c-344">Geometry GeometryType</span></span>
4.  <span data-ttu-id="efb4c-345">ApertureSize Integer in millimetri</span><span class="sxs-lookup"><span data-stu-id="efb4c-345">ApertureSize integer in millimeters</span></span>

<span data-ttu-id="efb4c-346">Le impostazioni predefinite sono:</span><span class="sxs-lookup"><span data-stu-id="efb4c-346">Defaults are:</span></span>

1.  <span data-ttu-id="efb4c-347">Stampanti RGB e CMYK:</span><span class="sxs-lookup"><span data-stu-id="efb4c-347">RGB and CMYK Printers:</span></span>
    1.  <span data-ttu-id="efb4c-348">MeasurementSpaceType CIE XYZ</span><span class="sxs-lookup"><span data-stu-id="efb4c-348">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="efb4c-349">WhitePointValue D50</span><span class="sxs-lookup"><span data-stu-id="efb4c-349">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="efb4c-350">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="efb4c-350">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="efb4c-351">ApertureSize 10mm</span><span class="sxs-lookup"><span data-stu-id="efb4c-351">10mm ApertureSize</span></span>
2.  <span data-ttu-id="efb4c-352">Scanner</span><span class="sxs-lookup"><span data-stu-id="efb4c-352">Scanners:</span></span>
    1.  <span data-ttu-id="efb4c-353">MeasurementSpaceType CIE XYZ</span><span class="sxs-lookup"><span data-stu-id="efb4c-353">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="efb4c-354">WhitePointValue D50</span><span class="sxs-lookup"><span data-stu-id="efb4c-354">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="efb4c-355">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="efb4c-355">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="efb4c-356">ApertureSize 10mm</span><span class="sxs-lookup"><span data-stu-id="efb4c-356">10mm ApertureSize</span></span>
3.  <span data-ttu-id="efb4c-357">Visualizza e dispositivo virtuale RGB:</span><span class="sxs-lookup"><span data-stu-id="efb4c-357">Displays and RGB Virtual Device:</span></span>
    1.  <span data-ttu-id="efb4c-358">MeasurementSpaceType CIE XYZ</span><span class="sxs-lookup"><span data-stu-id="efb4c-358">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="efb4c-359">WhitePointValue D65</span><span class="sxs-lookup"><span data-stu-id="efb4c-359">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="efb4c-360">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="efb4c-360">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="efb4c-361">ApertureSize 10mm</span><span class="sxs-lookup"><span data-stu-id="efb4c-361">10mm ApertureSize</span></span>
4.  <span data-ttu-id="efb4c-362">Fotocamere</span><span class="sxs-lookup"><span data-stu-id="efb4c-362">Cameras:</span></span>
    1.  <span data-ttu-id="efb4c-363">MeasurementSpaceType CIE XYZ</span><span class="sxs-lookup"><span data-stu-id="efb4c-363">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="efb4c-364">WhitePointValue D65</span><span class="sxs-lookup"><span data-stu-id="efb4c-364">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="efb4c-365">GeometryType diretto</span><span class="sxs-lookup"><span data-stu-id="efb4c-365">Direct GeometryType</span></span>
    4.  <span data-ttu-id="efb4c-366">ApertureSize 10mm</span><span class="sxs-lookup"><span data-stu-id="efb4c-366">10mm ApertureSize</span></span>

<span data-ttu-id="efb4c-367">**Condizioni di convalida:** La convalida di ogni sottoelemento è determinata dalle condizioni di convalida per tali sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-367">**Validation conditions:** Validation of each sub-element is determined by validation conditions for those sub-elements.</span></span> <span data-ttu-id="efb4c-368">Se manca un sottoelemento, viene usato il tipo di modello di dispositivo predefinito specifico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-368">If any sub-element is missing, the device model type specific default is used.</span></span>

### <a name="geometrytype"></a><span data-ttu-id="efb4c-369">GeometryType</span><span class="sxs-lookup"><span data-stu-id="efb4c-369">GeometryType</span></span>

<span data-ttu-id="efb4c-370">string</span><span class="sxs-lookup"><span data-stu-id="efb4c-370">String</span></span>

<span data-ttu-id="efb4c-371">Valori di enumerazione:</span><span class="sxs-lookup"><span data-stu-id="efb4c-371">Enumeration values:</span></span>

-   <span data-ttu-id="efb4c-372">"0/45"</span><span class="sxs-lookup"><span data-stu-id="efb4c-372">"0/45"</span></span>
-   <span data-ttu-id="efb4c-373">"0/diffuso"</span><span class="sxs-lookup"><span data-stu-id="efb4c-373">"0/diffuse"</span></span>
-   <span data-ttu-id="efb4c-374">"diffuso/0"</span><span class="sxs-lookup"><span data-stu-id="efb4c-374">"diffuse/0"</span></span>
-   <span data-ttu-id="efb4c-375">Diretto</span><span class="sxs-lookup"><span data-stu-id="efb4c-375">"Direct"</span></span>

<span data-ttu-id="efb4c-376">**Condizioni di convalida:** Qualsiasi valore, ad eccezione dei valori enumberation elencati, non è valido.</span><span class="sxs-lookup"><span data-stu-id="efb4c-376">**Validation conditions:** Any value except the enumberation values listed is invalid.</span></span> <span data-ttu-id="efb4c-377">Queste informazioni non modificheranno il comportamento di elaborazione della linea di base.</span><span class="sxs-lookup"><span data-stu-id="efb4c-377">This information will not change baseline processing behavior.</span></span>

### <a name="rgbprimariesgroup"></a><span data-ttu-id="efb4c-378">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="efb4c-378">RGBPrimariesGroup</span></span>

<span data-ttu-id="efb4c-379">Questo elemento è una sequenza di</span><span class="sxs-lookup"><span data-stu-id="efb4c-379">This element is a sequence of</span></span>

1.  <span data-ttu-id="efb4c-380">WhitePrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-380">WhitePrimary NonNegativeXYZType</span></span>
2.  <span data-ttu-id="efb4c-381">RedPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-381">RedPrimary NonNegativeXYZType</span></span>
3.  <span data-ttu-id="efb4c-382">GreenPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-382">GreenPrimary NonNegativeXYZType</span></span>
4.  <span data-ttu-id="efb4c-383">BluePrimary NonNegativeXYZTYpe</span><span class="sxs-lookup"><span data-stu-id="efb4c-383">BluePrimary NonNegativeXYZTYpe</span></span>
5.  <span data-ttu-id="efb4c-384">BlackPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-384">BlackPrimary NonNegativeXYZType</span></span>

<span data-ttu-id="efb4c-385">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-385">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyksampletype"></a><span data-ttu-id="efb4c-386">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="efb4c-386">NonNegativeCMYKSampleType</span></span>

<span data-ttu-id="efb4c-387">Questo elemento è una sequenza di</span><span class="sxs-lookup"><span data-stu-id="efb4c-387">This element is a sequence of</span></span>

1.  <span data-ttu-id="efb4c-388">NonNegativeCMYKType CMYK</span><span class="sxs-lookup"><span data-stu-id="efb4c-388">CMYK NonNegativeCMYKType</span></span>
2.  <span data-ttu-id="efb4c-389">NonNegativeXYZType CIE XYZ</span><span class="sxs-lookup"><span data-stu-id="efb4c-389">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="efb4c-390">L'elemento include anche una stringa di Tag Attribute facoltativa</span><span class="sxs-lookup"><span data-stu-id="efb4c-390">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="efb4c-391">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-391">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbsampletype"></a><span data-ttu-id="efb4c-392">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="efb4c-392">NonNegativeRGBSampleType</span></span>

<span data-ttu-id="efb4c-393">Questo elemento è una sequenza di</span><span class="sxs-lookup"><span data-stu-id="efb4c-393">This element is a sequence of</span></span>

1.  <span data-ttu-id="efb4c-394">NonNegativeRGBType RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-394">RGB NonNegativeRGBType</span></span>
2.  <span data-ttu-id="efb4c-395">NonNegativeXYZType CIE XYZ</span><span class="sxs-lookup"><span data-stu-id="efb4c-395">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="efb4c-396">L'elemento include anche una stringa di Tag Attribute facoltativa</span><span class="sxs-lookup"><span data-stu-id="efb4c-396">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="efb4c-397">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-397">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyktype"></a><span data-ttu-id="efb4c-398">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="efb4c-398">NonNegativeCMYKType</span></span>

<span data-ttu-id="efb4c-399">Questo elemento è costituito da attributi</span><span class="sxs-lookup"><span data-stu-id="efb4c-399">This element consisting of attributes</span></span>

1.  <span data-ttu-id="efb4c-400">C float</span><span class="sxs-lookup"><span data-stu-id="efb4c-400">C float</span></span>
2.  <span data-ttu-id="efb4c-401">Float M</span><span class="sxs-lookup"><span data-stu-id="efb4c-401">M float</span></span>
3.  <span data-ttu-id="efb4c-402">Float Y</span><span class="sxs-lookup"><span data-stu-id="efb4c-402">Y float</span></span>
4.  <span data-ttu-id="efb4c-403">K float</span><span class="sxs-lookup"><span data-stu-id="efb4c-403">K float</span></span>

<span data-ttu-id="efb4c-404">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-404">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbtype"></a><span data-ttu-id="efb4c-405">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="efb4c-405">NonNegativeRGBType</span></span>

<span data-ttu-id="efb4c-406">Questo elemento è costituito da attributi</span><span class="sxs-lookup"><span data-stu-id="efb4c-406">This element consisting of attributes</span></span>

1.  <span data-ttu-id="efb4c-407">Float R</span><span class="sxs-lookup"><span data-stu-id="efb4c-407">R float</span></span>
2.  <span data-ttu-id="efb4c-408">G float</span><span class="sxs-lookup"><span data-stu-id="efb4c-408">G float</span></span>
3.  <span data-ttu-id="efb4c-409">Float B</span><span class="sxs-lookup"><span data-stu-id="efb4c-409">B float</span></span>

<span data-ttu-id="efb4c-410">**Condizioni di convalida:** Per essere determinato dal feedback del settore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-410">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="extensiontype"></a><span data-ttu-id="efb4c-411">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="efb4c-411">ExtensionType</span></span>

<span data-ttu-id="efb4c-412">L'elemento ExtensionType è una sequenza di qualsiasi tipo di sottoelemento e viene usato per informazioni proprietarie da applicazioni non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efb4c-412">The ExtensionType element is a sequence of any sub-element type and is used for proprietary information from non-Microsoft applications.</span></span>

<span data-ttu-id="efb4c-413">**Condizioni di convalida:** Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-413">**Validation conditions:** This element is optional.</span></span> <span data-ttu-id="efb4c-414">Possono essere presenti al massimo 1000 sottoelementi di estensione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-414">There can be a maximum of 1000 extension sub-elements.</span></span>

### <a name="nonnegativexyztype"></a><span data-ttu-id="efb4c-415">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-415">NonNegativeXYZType</span></span>

<span data-ttu-id="efb4c-416">L'elemento NonNegativeXYZType è costituito da NonNegativeFloatType tre elementi a virgola mobile IEEE a precisione singola denominati "X", "Y" e "Z".</span><span class="sxs-lookup"><span data-stu-id="efb4c-416">The NonNegativeXYZType element is composed of NonNegativeFloatType three single-precision IEEE floating-point elements named "X," "Y," and "Z."</span></span> <span data-ttu-id="efb4c-417">Questi valori sono limitati ai valori di misurazione dei profili DMP.</span><span class="sxs-lookup"><span data-stu-id="efb4c-417">These values are limited to the DMP profiles measurement values.</span></span> <span data-ttu-id="efb4c-418">Queste misurazioni possono essere di tipo assoluto (non relativo) CIE XYZ 1931 o assoluti (non relativi) CIE XYZ 1931 Direct (transmissal) in candele per metro unità quadrate.</span><span class="sxs-lookup"><span data-stu-id="efb4c-418">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="efb4c-419">**Condizioni di convalida:** Solo i valori reali sono validi e i valori di misurazione CIE XYZ negativi non sono validi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-419">**Validation conditions:** Only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="efb4c-420">Poiché si tratta di valori assoluti, i valori possono essere maggiori di 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="efb4c-420">Because these are absolute values, values can be greater than 1.0f.</span></span> <span data-ttu-id="efb4c-421">Limite ragionevole per qualsiasi "X", "Y" o "Z".</span><span class="sxs-lookup"><span data-stu-id="efb4c-421">A reasonable limit for any "X," "Y," or "Z."</span></span> <span data-ttu-id="efb4c-422">il valore è arbitrariamente impostato su 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="efb4c-422">value is arbitrarily set to 10000.0f.</span></span>

### <a name="xyztype"></a><span data-ttu-id="efb4c-423">XYZType</span><span class="sxs-lookup"><span data-stu-id="efb4c-423">XYZType</span></span>

<span data-ttu-id="efb4c-424">L'elemento XYZType è costituito da tre valori a virgola mobile IEEE con precisione singola: "X", "Y" e "Z".</span><span class="sxs-lookup"><span data-stu-id="efb4c-424">The XYZType element is composed of three single-precision IEEE floating-point values: "X," "Y," and "Z."</span></span>

## <a name="the-cdmp-baseline-algorithms"></a><span data-ttu-id="efb4c-425">Algoritmi di base di CDMP</span><span class="sxs-lookup"><span data-stu-id="efb4c-425">The CDMP Baseline Algorithms</span></span>

### <a name="crt-device-model-baseline"></a><span data-ttu-id="efb4c-426">Baseline modello di dispositivo CRT</span><span class="sxs-lookup"><span data-stu-id="efb4c-426">CRT Device Model Baseline</span></span>

<span data-ttu-id="efb4c-427">Per comprendere questo modello, è necessario considerare sia il processo di caratterizzazione che la modellazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-427">To understand this model, you must consider both the characterization process and the device modeling.</span></span> <span data-ttu-id="efb4c-428">Nel processo di caratterizzazione, le misurazioni XYZ vengono eseguite prima sui colori ottenuti riempiendo il buffer di visualizzazione di un dispositivo di visualizzazione CRT.</span><span class="sxs-lookup"><span data-stu-id="efb4c-428">In the characterization process, XYZ measurements are first performed on the colors obtained by filling the display buffer of a CRT display device.</span></span> <span data-ttu-id="efb4c-429">I valori di esempio seguenti genereranno dati validi per il modello di dispositivo CRT Baseline:</span><span class="sxs-lookup"><span data-stu-id="efb4c-429">The following example values will generate good data for the baseline CRT device model:</span></span>

<span data-ttu-id="efb4c-430">Rosso: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="efb4c-431">Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="efb4c-432">Blu: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="efb4c-433">Neutrals: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255</span><span class="sxs-lookup"><span data-stu-id="efb4c-433">Neutrals: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255</span></span>

<span data-ttu-id="efb4c-434">È inoltre possibile utilizzare incrementi diversi da 15 e incrementi non lineari.</span><span class="sxs-lookup"><span data-stu-id="efb4c-434">Increments other than 15 and nonlinear increments can also be used.</span></span> <span data-ttu-id="efb4c-435">Ogni rampa rossa, verde, blu e neutra deve contenere almeno tre campioni, ma è consigliabile fornire più esempi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-435">Each red, green, blue, and neutral ramp must contain at least three samples, but providing more samples is recommended.</span></span> <span data-ttu-id="efb4c-436">È necessario fornire esempi per i puri rossi, verdi, blu, neri e bianchi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-436">You must provide samples for pure red, green, blue, black, and white.</span></span> <span data-ttu-id="efb4c-437">Gli esempi non devono essere distanziati in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="efb4c-437">The samples do not have to be uniformly spaced.</span></span>

<span data-ttu-id="efb4c-438">Il processo di creazione della matrice tristimolo è costituito da due passaggi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-438">The process of building the tristimulus matrix consists of two steps.</span></span> <span data-ttu-id="efb4c-439">Per prima cosa, stimare il valore XYZ del punto nero o il bagliore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-439">First, estimate the black point XYZ value, or the flare.</span></span> <span data-ttu-id="efb4c-440">Questo passaggio si basa in larga misura sul lavoro di Bernas \[ 3 \] con una funzione oggettiva leggermente modificata per l'ottimizzazione non lineare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-440">This step is based largely on work of Berns\[3\] with a slightly modified objective function for the nonlinear optimization.</span></span> <span data-ttu-id="efb4c-441">In secondo luogo, calcolare la matrice tristimolo in base al risultato del passaggio uno e anche da un calcolo della media di tutte le misurazioni per canale, non solo da quello per il numero massimo di numeri digitali.</span><span class="sxs-lookup"><span data-stu-id="efb4c-441">Second, calculate tristimulus matrix based on the result from step one and also from an averaging calculation on all of the per-channel measurements, not just the one for maximum digital count.</span></span>

<span data-ttu-id="efb4c-442">Ognuno di questi passaggi contiene procedure dettagliate.</span><span class="sxs-lookup"><span data-stu-id="efb4c-442">Each of these steps contains detailed procedures.</span></span> <span data-ttu-id="efb4c-443">Il punto di partenza è costituito dalle rampe (17 passaggi nell'esempio) per ogni canale R, G e B.</span><span class="sxs-lookup"><span data-stu-id="efb4c-443">The starting point is the ramps (17 steps in our example) for each of R, G, and B channels.</span></span> <span data-ttu-id="efb4c-444">Quando le misurazioni XYZ sono tracciate sul piano *XY* di cromaticità, una situazione tipica è illustrata nella figura 1.</span><span class="sxs-lookup"><span data-stu-id="efb4c-444">When the XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="efb4c-445">Il primo passaggio consiste nella risoluzione di un problema di ottimizzazione non lineare per individuare il punto nero "migliore adattamento" che ridurrà al minimo la tendenza nella cromaticità come uno attraversa lungo i canali R, G e B.</span><span class="sxs-lookup"><span data-stu-id="efb4c-445">Step one consists of solving a nonlinear optimization problem to find the "best fit" black point that will minimize the drift in chromaticity as one traverses along the R, G, and B channels.</span></span> <span data-ttu-id="efb4c-446">In base a Bernas \[ 3, cerchiamo \] ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ) che riduce al minimo la funzione Objective seguente:</span><span class="sxs-lookup"><span data-stu-id="efb4c-446">Based on Berns\[3\], we seek ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ) that minimizes the following objective function:</span></span>

![Mostra la funzione objective in cui SR, SG e SB sono il set di punti dati nei canali R, G e B.](images/cdmp-formula1.png)

<span data-ttu-id="efb4c-448">dove *s <sub>R</sub>*,*s <sub>G</sub>* e *s <sub>B</sub>* sono il set di punti dati corrispondente ai punti sui canali R, G e b.</span><span class="sxs-lookup"><span data-stu-id="efb4c-448">where *S <sub>R</sub>*,*S <sub>G</sub>*, and *S<sub>B</sub>* are the set of data points corresponding to the points on the R, G, and B channels.</span></span> <span data-ttu-id="efb4c-449">Per qualsiasi set *S*, definire:</span><span class="sxs-lookup"><span data-stu-id="efb4c-449">For any set *S*, define:</span></span>

![Mostra una formula per la definizione di tutti i set.](images/cdmp-formula2.png)

<span data-ttu-id="efb4c-451">Nell'esempio precedente, \| *s* \| è la cardinalità di *s*, ovvero il numero di punti nel set *S*. ![ Mostra una formula per la cromaticità di un punto.](images/cdmp-formula3.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-451">In the preceding, \| *S* \| is the cardinality of *S*, i.e., the number of points in the set *S*. ![Shows a formula for the chromaticity of a point.](images/cdmp-formula3.png)</span></span> <span data-ttu-id="efb4c-452">Coordinate di cromaticità del punto che ![ Mostra un formaula per un punto.](images/cdmp-formula4.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-452">is the chromaticity coordinates of the point ![Shows a formaula for a point.](images/cdmp-formula4.png)</span></span> <span data-ttu-id="efb4c-453">, quindi, ![ Mostra una formula per la media o il centro della massa. ](images/cdmp-formula5.png) , è la media, o il centro della massa, di tutti i punti nel set *S* nel piano di cromaticità.</span><span class="sxs-lookup"><span data-stu-id="efb4c-453">, so ![Shows a formula for the average or center of mass.](images/cdmp-formula5.png), is the average, or center of mass, of all the points in the set *S* in the chromaticity plane.</span></span> <span data-ttu-id="efb4c-454">Quindi, ![ Mostra una formula per la somma di un secondo istanti di punti.](images/cdmp-formula6.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-454">Thus, ![Shows a formula for the sum of a second moments of points.](images/cdmp-formula6.png)</span></span> <span data-ttu-id="efb4c-455">è la somma di secondi di punti relativi al centro della massa ed è una misura della diffusione dei punti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-455">is the sum of second moments of the points about the center of mass and is a measure of how spread out the points are about it.</span></span> <span data-ttu-id="efb4c-456">Infine, ![ Mostra una formula per la misura totale della distribuzione di tre cluster di punti.](images/cdmp-formula7.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-456">Finally, ![Shows a formula for the total measure of the spread of three clusters of points.](images/cdmp-formula7.png)</span></span> <span data-ttu-id="efb4c-457">è una misura totale di come la distribuzione dei tre cluster di punti riguarda i rispettivi centri di massa.</span><span class="sxs-lookup"><span data-stu-id="efb4c-457">is a total measure of how spread out the three clusters of points are about their respective centers of mass.</span></span>

<span data-ttu-id="efb4c-458">Nel calcolo di ![ viene mostrata una formula di f (X, Y, Z; XK,, di ZK, ZK).](images/cdmp-formula8.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-458">In the calculation of ![Shows a formula of f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png)</span></span> <span data-ttu-id="efb4c-459">, se ![ Mostra una formula per X. ](images/cdmp-formula9.png) , il calcolo viene ignorato e la cardinalità di *S* viene modificata di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="efb4c-459">, if ![Shows a formula for X.](images/cdmp-formula9.png) , then the calculation is skipped, and the cardinality of *S* is adjusted accordingly.</span></span>

<span data-ttu-id="efb4c-460">Nonostante la complessità apparente della funzione oggettiva, è una somma dei quadrati di molte funzioni differenziabili in *X <sub>k</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 punti 2 *XY* -Components 3 Channels = 102, nell'esempio) e, pertanto, è suscettibile alle tecniche standard non lineari minime, ad esempio l'algoritmo Levenberg-Marquardt, che è l'algoritmo usato in WCS.</span><span class="sxs-lookup"><span data-stu-id="efb4c-460">Despite the apparent complexity of the objective function, it is a sum of the squares of many differentiable functions in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 points   2 *xy* -components   3 channels = 102, in the example), and, therefore, is amenable to standard nonlinear least squares techniques, such as the Levenberg-Marquardt algorithm, which is the algorithm used in WCS.</span></span> <span data-ttu-id="efb4c-461">Si noti che la funzione dell'obiettivo precedente è diversa da quella suggerita in Bernas \[ 3 \] in quanto quest'ultima misura la varianza delle distanze dal centro della massa, in modo che la varianza sia zero quando i punti sono equidistanti dal centro della massa, anche se possono diffondersi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-461">Note that the preceding objective function is different from the one suggested in Berns\[3\] in that the latter function measures the variance of the distances from the center of mass, so that the variance is zero when the points are equidistant from the center of mass, even though they may spread out quite a bit about it.</span></span> <span data-ttu-id="efb4c-462">Nell'esempio, la dispersione dei punti è contollata direttamente usando i secondi istanti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-462">In the example, the dispersion of points is contolled directly using the second moments.</span></span>

<span data-ttu-id="efb4c-463">Come per qualsiasi algoritmo iterativo per il problema dei minimi quadrati non lineari, Levenberg-Marquardt richiede una supposizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="efb4c-463">As with any iterative algorithm for the nonlinear least squares problem, Levenberg-Marquardt requires an initial guess.</span></span> <span data-ttu-id="efb4c-464">Esistono due candidati evidenti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-464">There are two obvious candidates.</span></span> <span data-ttu-id="efb4c-465">Uno è (0, 0, 0); l'altro è il punto nero misurato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-465">One is (0, 0, 0); the other is the measured black point.</span></span> <span data-ttu-id="efb4c-466">Per la CTE, il punto nero misurato viene usato per la prima volta come supposizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="efb4c-466">For the CTE, the measured black point is first used as the initial guess.</span></span> <span data-ttu-id="efb4c-467">Se viene superato un massimo di 100 iterazioni senza raggiungere una soglia di una distanza media di 0,001 di ogni punto dal centro di massa (che corrisponde a un valore soglia di (0,001) 17 3 = 0,000051 per la funzione Objective), viene eseguito un altro ciclo di iterazioni con l'ipotesi iniziale di (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="efb4c-467">If a maximum of 100 iterations is exceeded without achieving a threshold of an average distance of 0.001 of each point from its center of mass (which corresponds to a threshold value of (0.001)    17   3 = 0.000051 for the objective function), then another round of iterations with the initial guess of (0, 0, 0) is performed.</span></span> <span data-ttu-id="efb4c-468">La stima risultante del punto nero è XYZ rispetto alla stima migliore del ciclo di iterazione precedente (con il punto nero misurato come supposizione iniziale).</span><span class="sxs-lookup"><span data-stu-id="efb4c-468">The resulting estimate of the black point is XYZ compared with the best estimate from the previous round of iterations (with the measured black point as the initial guess).</span></span> <span data-ttu-id="efb4c-469">Utilizzare la stima che fornisce il valore più piccolo per la funzione Objective.</span><span class="sxs-lookup"><span data-stu-id="efb4c-469">Use the estimate that gives the smallest value for the objective function.</span></span> <span data-ttu-id="efb4c-470">La scelta di iterazioni 100 e la distanza degli errori di 0,001 sono state selezionate empiricamente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-470">The choice of 100 iterations and the error distance of 0.001 were each selected empirically.</span></span> <span data-ttu-id="efb4c-471">Nelle versioni future, potrebbe essere ragionevole parametrizzare la distanza degli errori.</span><span class="sxs-lookup"><span data-stu-id="efb4c-471">In future versions, it might be reasonable to parameterize the error distance.</span></span>

<span data-ttu-id="efb4c-472">Il risultato del passaggio uno è il punto nero stimato ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="efb4c-472">The result of step one is the estimated black point ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ).</span></span> <span data-ttu-id="efb4c-473">Il secondo passaggio consiste nel determinare la matrice tristimolo calcolando la media della cromaticità dei punti nei tre cluster ottenuti nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="efb4c-473">Step two consists of determining the tristimulus matrix by averaging the chromaticity of the points in the three clusters obtained in step one.</span></span> <span data-ttu-id="efb4c-474">Per CRT, questa operazione viene eseguita principalmente per ridurre al minimo gli effetti degli errori di misurazione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-474">For CRTs, this is done primarily to minimize the effects of measurement errors.</span></span> <span data-ttu-id="efb4c-475">I punti usati per la media della cromaticità devono essere gli stessi punti usati nell'ottimizzazione nel passaggio uno.</span><span class="sxs-lookup"><span data-stu-id="efb4c-475">The points used in averaging the chromaticity must be the same points used in the optimization in step one.</span></span> <span data-ttu-id="efb4c-476">In altre parole, se il primo punto (Digital count 15, nell'esempio) in ogni rampa viene eliminato nel passaggio di ottimizzazione, lo stesso deve essere eseguito nella media.</span><span class="sxs-lookup"><span data-stu-id="efb4c-476">In other words, if the first point (digital count 15, in the example) in each ramp is discarded in the optimization step, then the same must be done in the averaging.</span></span> <span data-ttu-id="efb4c-477">Se ![ Mostra le formule della cromaticità media per le coordinate nei canali rosso e verde.](images/cdmp-formula10.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-477">If ![Shows formulas of averaged chromaticity for coordinates in the red and green channels.](images/cdmp-formula10.png)</span></span> <span data-ttu-id="efb4c-478">e ![ Mostra una formula della cromaticità media per le coordinate nel canale blu.](images/cdmp-formula11.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-478">, and ![Shows a formula of averaged chromaticity for coordinates in the blue channel.](images/cdmp-formula11.png)</span></span> <span data-ttu-id="efb4c-479">sono le coordinate della cromaticità media dei canali rosso, verde e blu, quindi la procedura seguente determina la matrice tristimolo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-479">are the averaged chromaticity coordinates of the red, green, and blue channels, then the following procedure determines the tristimulus matrix.</span></span> <span data-ttu-id="efb4c-480">Per prima cosa, risolvere il 3? 3 sistema lineare:</span><span class="sxs-lookup"><span data-stu-id="efb4c-480">First, solve the 3?3 linear system:</span></span>

![Mostra la prima parte della procedura per risolvere un sistema lineare 3? 3.](images/cdmp-formula12.png)

![Mostra la seconda parte del sistema lineare 3? 3.](images/cdmp-formula13.gif)![Mostra il valore di t pedice b alla fine della seconda parte del sistema lineare 3? 3.](images/cdmp-formula14.gif)

<span data-ttu-id="efb4c-484">*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>w</sub>*</span><span class="sxs-lookup"><span data-stu-id="efb4c-484">*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z<sub>W</sub>*</span></span>

![Mostra la parte finale della procedura per risolvere un sistema lineare 3? 3.](images/cdmp-formula15.png)

<span data-ttu-id="efb4c-486">Dopo che la matrice tristimolo è stata determinata, la determinazione delle curve di tono segue l'approccio standard.</span><span class="sxs-lookup"><span data-stu-id="efb4c-486">After the tristimulus matrix is determined, the determination of tone curves follows the standard approach.</span></span> <span data-ttu-id="efb4c-487">Per le visualizzazioni CRT, si presuppone che i singoli canali seguano il modello "GOG":</span><span class="sxs-lookup"><span data-stu-id="efb4c-487">For CRT displays, the individual channels are assumed to follow the "GOG" model:</span></span>

![Mostra la formula per il modello ' G O G '.](images/cdmp-formula16.png)

<span data-ttu-id="efb4c-489">dove *k <sub>g</sub>* è il "guadagno", 1-*k <sub>g</sub>* è "offset" e?</span><span class="sxs-lookup"><span data-stu-id="efb4c-489">where *k <sub>g</sub>* is the "gain",1 -*k<sub>g</sub>* is the "offset", and ?</span></span> <span data-ttu-id="efb4c-490">è il "gamma".</span><span class="sxs-lookup"><span data-stu-id="efb4c-490">is the "gamma."</span></span> <span data-ttu-id="efb4c-491">La matrice inversa della matrice tristimolo viene applicata ai dati XYZ degli neutri per ottenere i dati RGB lineari, che vengono quindi correlati con i valori RGB digitali usando la regressione non lineare sul modello GOG.</span><span class="sxs-lookup"><span data-stu-id="efb4c-491">The inverse matrix of the tristimulus matrix is applied to the XYZ data of the neutrals to obtain the linear RGB data, which is then correlated with the digital RGB values using nonlinear regression on the GOG model.</span></span> <span data-ttu-id="efb4c-492">Queste caratteristiche non devono essere uguali per i canali R, G e B e in genere non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="efb4c-492">These characteristics do not have to be the same for the R, G, and B channels, and generally are not the same.</span></span>

<span data-ttu-id="efb4c-493">Berns \[ 1 \] : Berns, *Billmeyer e spugnos, principi della tecnologia dei colori*, 3 <sub>Rd</sub> ed.</span><span class="sxs-lookup"><span data-stu-id="efb4c-493">Berns\[1\]: Berns, *Billmeyer and Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed.</span></span> <span data-ttu-id="efb4c-494">John Wiley & Sons (2000).</span><span class="sxs-lookup"><span data-stu-id="efb4c-494">John Wiley & Sons (2000).</span></span>

<span data-ttu-id="efb4c-495">Berns \[ 2 \] : Berns e Katoh, la funzione di trasferimento da digitale a radiometrica per i monitor CRT controllati da computer, il *Simposio esperto cie di 97 colori standard per la tecnologia di imaging*, nov. 1997.</span><span class="sxs-lookup"><span data-stu-id="efb4c-495">Berns\[2\]: Berns and Katoh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97 Colour Standards for Imaging Technology*, Nov. 1997.</span></span>

<span data-ttu-id="efb4c-496">Berns \[ 3 \] : Bernas, Fernandez e Taplin, stima Black-Level le emissioni di Computer-Controlled Visualizzazioni, *ricerca a colori e applicazione*, 28:379-383 dei periodici Wiley, Inc. (2003)</span><span class="sxs-lookup"><span data-stu-id="efb4c-496">Berns\[3\]: Berns, Fernandez and Taplin, Estimating Black-Level Emissions of Computer-Controlled Displays, *Color Research and Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)</span></span>

<span data-ttu-id="efb4c-497">Kang \[ 1 \] : Kang, *tecnologia dei colori per dispositivi di imaging elettronico*, spie (1997)</span><span class="sxs-lookup"><span data-stu-id="efb4c-497">Kang\[1\]: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)</span></span>

<span data-ttu-id="efb4c-498">Katoh \[ 1 \] : Katoh, Deguchi e Berns, una descrizione accurata della proposta di monitoraggio CRT (II) per un'estensione del metodo CIE e la relativa verifica, *opt. Rev.* 8:397-408 (2001)</span><span class="sxs-lookup"><span data-stu-id="efb4c-498">Katoh\[1\]: Katoh, Deguchi and Berns, An accurate characterization of CRT monitor (II) proposal for an extension to CIE method and its verification, *Opt. Rev.* 8: 397-408 (2001)</span></span>

### <a name="lcd-device-model-baseline"></a><span data-ttu-id="efb4c-499">Linea di base del modello di dispositivo LCD</span><span class="sxs-lookup"><span data-stu-id="efb4c-499">LCD Device Model Baseline</span></span>

<span data-ttu-id="efb4c-500">La linea di base del modello di dispositivo LCD è simile alla baseline del modello di dispositivo CRT.</span><span class="sxs-lookup"><span data-stu-id="efb4c-500">The LCD Device Model Baseline is similar to the CRT Device Model Baseline.</span></span> <span data-ttu-id="efb4c-501">In questa sezione vengono illustrati i modi in cui la modellazione LCD è diversa dalla modellazione CRT.</span><span class="sxs-lookup"><span data-stu-id="efb4c-501">This section will explain the ways in which LCD modeling differs from CRT modeling.</span></span>

<span data-ttu-id="efb4c-502">Una differenza consiste nel fatto che non è possibile presupporre che gli schermi LCD seguano il modello GOG usato per CRT e che le curve di tono siano ottenute dall'interpolazione dei dati misurati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-502">One difference is that you cannot assume that LCD displays follow the GOG model used for CRTs, and the tone curves are obtained by interpolation of measured data.</span></span> <span data-ttu-id="efb4c-503">Per questo motivo, è consigliabile campionare l'asse neutro del dispositivo con maggiore frequenza.</span><span class="sxs-lookup"><span data-stu-id="efb4c-503">Because of that, the device neutral axis should be sampled more frequently.</span></span>

<span data-ttu-id="efb4c-504">Di seguito sono riportati alcuni valori di esempio tipici che possono generare dati validi per la baseline del modello di dispositivo LCD:</span><span class="sxs-lookup"><span data-stu-id="efb4c-504">Here are some typical example values that can generate good data for the LCD device model baseline:</span></span>

<span data-ttu-id="efb4c-505">Rosso: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="efb4c-506">Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="efb4c-507">Blu: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="efb4c-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span><span class="sxs-lookup"><span data-stu-id="efb4c-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span></span>

<span data-ttu-id="efb4c-509">Il processo di media delle cromie di colore misurato per ottenere la cromaticità per le primarie del dispositivo è più importante per gli LCD rispetto a CRT.</span><span class="sxs-lookup"><span data-stu-id="efb4c-509">The process of averaging measured color chromaticies to obtain the chromaticities for the device primaries is more critical for LCDs than it is for CRTs.</span></span> <span data-ttu-id="efb4c-510">Quando le misurazioni XYZ sono tracciate sulla superficie *XY* , una situazione tipica è illustrata nella figura 1.</span><span class="sxs-lookup"><span data-stu-id="efb4c-510">When XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="efb4c-511">Si noti come la cromaticità si allontana verso il punto nero.</span><span class="sxs-lookup"><span data-stu-id="efb4c-511">Notice how the chromaticity drifts toward the black point.</span></span> <span data-ttu-id="efb4c-512">Questo perché tutti gli LCD hanno una certa quantità di perdite di luce.</span><span class="sxs-lookup"><span data-stu-id="efb4c-512">This is because all LCDs have a certain amount of light leakage.</span></span>

![Diagramma che mostra un grafico della cromaticità utilizzando dati non elaborati senza correzione.](images/cdmp-lcd-dmp-figure1.png)

<span data-ttu-id="efb4c-514">**Figura 1** : diagramma di cromaticità con dati non elaborati senza correzione</span><span class="sxs-lookup"><span data-stu-id="efb4c-514">**Figure 1** : The chromaticity diagram using raw data with no correction</span></span>

<span data-ttu-id="efb4c-515">Quando viene sottratto dalle misurazioni XYZ non elaborate, una situazione tipica è illustrata nella figura 2.</span><span class="sxs-lookup"><span data-stu-id="efb4c-515">When this is subtracted from the raw XYZ measurements, a typical situation is depicted in Figure 2.</span></span> <span data-ttu-id="efb4c-516">I punti di TImpossibile sono ora raggruppati in tre centri, sebbene non rientrino in modo identico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-516">Tthe points are now clustered about three centers, although they don't fall identically on them.</span></span> <span data-ttu-id="efb4c-517">Il processo di mediazione descritto per CRT migliora notevolmente i risultati per i monitor LCD.</span><span class="sxs-lookup"><span data-stu-id="efb4c-517">The averaging process described for CRTs greatly improves the results for LCDs.</span></span>

![Diagramma che mostra un grafico della cromaticità utilizzando dati non elaborati con un punto nero modificato.](images/cdmp-lcd-dmp-figure2.png)

<span data-ttu-id="efb4c-519">**Figura 2** : diagramma di cromaticità con i dati con punto nero modificato</span><span class="sxs-lookup"><span data-stu-id="efb4c-519">**Figure 2** : The chromaticity diagram using data with adjusted black point</span></span>

### <a name="rgb-capture-device-model-baseline"></a><span data-ttu-id="efb4c-520">Linea di base modello di acquisizione RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-520">RGB Capture Device Model Baseline</span></span>

<span data-ttu-id="efb4c-521">Il modello di dispositivo di acquisizione RGB di base è una sottoclasse della classe IDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="efb4c-521">The baseline RGB capture device model is a subclass of the IDeviceModel class.</span></span> <span data-ttu-id="efb4c-522">Nella caratterizzazione colorimetrico dei dispositivi di acquisizione dei colori, ad esempio scanner e fotocamere digitali, viene usato l'approccio seguente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-522">In the colorimetric characterization of color capture devices, such as scanners and digital cameras, the following approach is used.</span></span> <span data-ttu-id="efb4c-523">Una destinazione costituita da patch di colore con valori CIE XYZ noti viene acquisita usando il dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-523">A target consisting of color patches with known CIEXYZ values is captured using the capture device.</span></span> <span data-ttu-id="efb4c-524">Il risultato dell'acquisizione è un'immagine bitmap RGB in cui il colore di ogni patch è codificato in un valore RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-524">The result of the capture is an RGB bitmap image in which the color of each patch is encoded in an RGB value.</span></span> <span data-ttu-id="efb4c-525">Questi valori RGB del dispositivo sono specifici di un dispositivo di acquisizione specifico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-525">These device RGB values are specific to a particular capture device.</span></span> <span data-ttu-id="efb4c-526">L'obiettivo della caratterizzazione colorimetrico è stabilire una relazione empirica tra i valori RGB del dispositivo e i valori CIE XYZ o una trasformazione matematica da RGB a XYZ che modella il più accuratamente possibile il comportamento del dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-526">The goal of colorimetric characterization is to establish an empirical relationship between the device RGB values and CIEXYZ values, or a mathematical transformation from RGB to XYZ that models as accurately as possible the behavior of the capture device.</span></span>

<span data-ttu-id="efb4c-527">Una trasformazione matematica di questo tipo può essere modellata ragionevolmente da polinomi di basso livello.</span><span class="sxs-lookup"><span data-stu-id="efb4c-527">Such a mathematical transformation can be modeled reasonably by polynomials of low degrees.</span></span> <span data-ttu-id="efb4c-528">Questa procedura è descritta in dettaglio in letteratura, ad esempio Kang \[ 92 \] , Kang \[ 97 \] .</span><span class="sxs-lookup"><span data-stu-id="efb4c-528">This procedure is detailed in the literature, for example Kang\[92\], Kang\[97\].</span></span> <span data-ttu-id="efb4c-529">In Kang \[ 97 \] viene segnalato un approccio che usa un set di tre polinomi con 3, 6, 8, 9, 11, 14 o 20 termini nelle variabili R, G e B, mentre i tre polinomi regressione rispettivamente nei componenti X, Y, Z dello spazio CIE XYZ.</span><span class="sxs-lookup"><span data-stu-id="efb4c-529">In Kang\[97\], an approach is reported that uses a set of three polynomials with 3, 6, 8, 9, 11, 14 or 20 terms in the R, G, and B variables, while the three polynomials regress respectively into the X, Y, Z components of the CIEXYZ space.</span></span> <span data-ttu-id="efb4c-530">Per il polinomio a 20 termini, il formato è:</span><span class="sxs-lookup"><span data-stu-id="efb4c-530">For the 20-term polynomial, the form is:</span></span>

![Mostra il polinomio a 20 termini.](images/cdmp-formula20.png)

<span data-ttu-id="efb4c-532">Sono presenti espressioni simili per Y e Z. La tecnica matematica per l'adattamento dei polinomi rientra in "regressione lineare multivariata" ed è descritta in qualsiasi testo elementare in Statistics.</span><span class="sxs-lookup"><span data-stu-id="efb4c-532">There are similar expressions for Y and Z. The mathematical technique for fitting the polynomials falls within "Multivariate Linear Regression" and is described in any elementary text in Statistics.</span></span>

<span data-ttu-id="efb4c-533">Questo metodo di regressione lineare soffre di non ridurre al minimo la funzione dell'obiettivo "Right".</span><span class="sxs-lookup"><span data-stu-id="efb4c-533">This method of linear regression suffers from not minimizing the "right" objective function.</span></span> <span data-ttu-id="efb4c-534">Per impostazione predefinita, la regressione lineare trova la soluzione dei minimi quadrati, che implica che i coefficienti ottenuti ridurranno al minimo la somma totale dei quadrati di errori nello spazio sottostante, o in modo equivalente, la somma dei quadrati delle distanze euclidee.</span><span class="sxs-lookup"><span data-stu-id="efb4c-534">By design, linear regression finds the least squares solution, which implies that the coefficients obtained will minimize the total sum of squares of errors in the underlying space, or equivalently, the sum of squares of the Euclidean distances.</span></span> <span data-ttu-id="efb4c-535">In pratica, si vuole ridurre al minimo la somma dei quadrati di? Es, dove? E è uno degli standard accettati, ad esempio CIE94.</span><span class="sxs-lookup"><span data-stu-id="efb4c-535">In practice, you want to minimize the sum of squares of ?Es, where ?E is one of the accepted standards such as CIE94.</span></span> <span data-ttu-id="efb4c-536">La riduzione di questa funzione oggettiva è un problema di regressione non lineare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-536">Minimizing this objective function is a nonlinear regression problem.</span></span>

<span data-ttu-id="efb4c-537">Nel nuovo motore, Lab per XYZ è lo spazio dei colori CIE in cui viene regressione e viene usato il polinomiale cubico a 20 termini come modello per il dispositivo di acquisizione, o coefficienti ls, come, BS, in modo che i polinomi seguenti riducano al minimo la somma dei quadrati di? E <sub>CIE94</sub> .</span><span class="sxs-lookup"><span data-stu-id="efb4c-537">In the new engine, Lab to XYZ is the CIE color space that is regressed into, and the 20-term cubic polynomial is used as the model for the capture device, or coefficients ls,as,bs such that the following polynomials minimize the sum of squares of ?E <sub>CIE94</sub> s.</span></span>

![Mostra un set di formule polinomiali.](images/cdmp-formula21.png)

<span data-ttu-id="efb4c-539">La soluzione ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) nello spazio numerico reale 60 dimensionale **R** 203 deve essere tale che l'errore totale seguente sia ridotto a icona:</span><span class="sxs-lookup"><span data-stu-id="efb4c-539">The solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) in the 60-dimensional real numeric space **R** 203 must be such that the following total error is minimized:</span></span>

![Mostra l'errore totale da ridurre a icona.](images/cdmp-formula22.png)

<span data-ttu-id="efb4c-541">dove la sommatoria è attraverso tutte le coppie di punti dati (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) nel set di dati campionati più punti di controllo aggiuntivi per essere descritti in dettaglio nell'esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="efb4c-541">where the summation is through all the data point pairs (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v<sub>i</sub>* ) in the sampled data set plus additional control points to be detailed in the following.</span></span> <span data-ttu-id="efb4c-542">Si tratta di un problema di regressione non lineare perché i parametri *?<sub> i</sub>*, *a <sub>i</sub>*, \* <sub>i</sub>\* entri nella funzione objective in modo non lineare (non quadratico).</span><span class="sxs-lookup"><span data-stu-id="efb4c-542">This is a nonlinear regression problem because the parameters *?<sub>i</sub>*, *a<sub>i</sub>*, \* <sub>i</sub>\* enter into the objective function in a nonlinear way (not quadratically).</span></span>

<span data-ttu-id="efb4c-543">Poiché la funzione Objective?</span><span class="sxs-lookup"><span data-stu-id="efb4c-543">Because the objective function ?</span></span> <span data-ttu-id="efb4c-544">è una funzione non lineare (e non quadratica) dei parametri *?<sub> i</sub>*, *a <sub>i</sub>* e \* <sub>i</sub>\* è necessario ricorrere a tecniche iterative per risolvere il problema di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-544">is a nonlinear (and nonquadratic) function of the parameters *?<sub>i</sub>*, *a<sub>i</sub>* and \* <sub>i</sub>\*, you must resort to iterative techniques to solve the optimization problem.</span></span> <span data-ttu-id="efb4c-545">Poiché il form della funzione Objective è una somma di quadrati, viene usata una tecnica di ottimizzazione standard denominata Levenberg-Marquardt algoritmo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-545">Because the form of the objective function is a sum of squares, a standard optimization technique called the Levenberg-Marquardt algorithm is used.</span></span> <span data-ttu-id="efb4c-546">Viene considerato il metodo preferito per i problemi non lineari con i minimi quadrati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-546">It is considered the method of choice for nonlinear least squares problems.</span></span> <span data-ttu-id="efb4c-547">Per gli algoritmi iterativi come Levenberg-Marquardt, è necessario fornire una supposizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="efb4c-547">For iterative algorithms such as Levenberg-Marquardt, you must supply an initial guess.</span></span> <span data-ttu-id="efb4c-548">Una buona supposizione iniziale è in genere cruciale nell'individuare il valore minimo corretto.</span><span class="sxs-lookup"><span data-stu-id="efb4c-548">A good initial guess is usually critical in finding the correct minimum value.</span></span> <span data-ttu-id="efb4c-549">In questo caso, un candidato valido per l'ipotesi iniziale è la soluzione del problema di regressione lineare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-549">In this case, one good candidate for the initial guess is the solution of the linear regression problem.</span></span> <span data-ttu-id="efb4c-550">Per prima cosa, ridurre al minimo la somma del quadrato delle distanze euclidee nello spazio Lab definendo una funzione di obiettivo quadratico:</span><span class="sxs-lookup"><span data-stu-id="efb4c-550">First, minimize the sum of the square of Euclidean distances in Lab space, by defining a quadratic objective function:</span></span>

![Mostra una funzione dell'obiettivo quadratico definita.](images/cdmp-formula23.png)

<span data-ttu-id="efb4c-552">La soluzione matematica a questo problema "lineare con i minimi quadrati" è nota.</span><span class="sxs-lookup"><span data-stu-id="efb4c-552">The mathematical solution to such "linear least squares" problem is well known.</span></span> <span data-ttu-id="efb4c-553">Perché *?<sub></sub>viene visualizzato solo nella* modellazione *L* , *a <sub>i</sub>* viene visualizzato solo nella modellazione *u* e \* <sub>i</sub>\* viene visualizzato solo nella modellazione *v* ; il problema di ottimizzazione può essere scomposto in tre problemi, uno per *L*, uno per *u* e uno per *v*.</span><span class="sxs-lookup"><span data-stu-id="efb4c-553">Because *?<sub>i</sub>* only appears in the *L* modeling, *a <sub>i</sub>* only appears in the *u* modeling, and \* <sub>i</sub>\* only appears in the *v* modeling; the optimization problem can be decomposed into three subproblems: one for *L*, one for *u* and one for *v*.</span></span> <span data-ttu-id="efb4c-554">Prendere in considerazione le equazioni *L* .</span><span class="sxs-lookup"><span data-stu-id="efb4c-554">Consider the *L* equations.</span></span> <span data-ttu-id="efb4c-555">(Le equazioni *u* e le equazioni *v* seguono esattamente lo stesso argomento). Il problema di ridurre al minimo la somma dei quadrati di errori in *L* può essere dichiarato come la risoluzione dell'equazione di matrice seguente nel senso minimo dei quadrati:</span><span class="sxs-lookup"><span data-stu-id="efb4c-555">(The *u* equations and the *v* equations follow exactly the same argument.) The problem of minimizing the sum of squares of errors in *L* can be stated as solving the following matrix equation in the least squares sense:</span></span>

![Mostra un'equazione della matrice per L.](images/cdmp-formula24.png)

<span data-ttu-id="efb4c-557">dove *N* è il numero totale di punti dati (punti campionati originali più punti di controllo creati in un modo descritto di seguito).</span><span class="sxs-lookup"><span data-stu-id="efb4c-557">where *N* is the total number of data points (original sampled points plus control points created in a manner described below).</span></span> <span data-ttu-id="efb4c-558">In genere, *N* è molto più grande di 20, quindi l'equazione precedente è troppo determinata, richiedendo una soluzione con almeno quadrati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-558">Typically, *N* is much larger than 20, so the preceding equation is over-determined, requiring a least squares solution.</span></span> <span data-ttu-id="efb4c-559">Una soluzione form chiusa per **?**</span><span class="sxs-lookup"><span data-stu-id="efb4c-559">A closed form solution for **?**</span></span> <span data-ttu-id="efb4c-560">disponibile:</span><span class="sxs-lookup"><span data-stu-id="efb4c-560">is available:</span></span>

![Mostra una soluzione form chiusa.](images/cdmp-formula25.png)

<span data-ttu-id="efb4c-562">In pratica, la valutazione diretta tramite la soluzione modulo chiuso non viene utilizzata perché contiene proprietà numeriche scarse.</span><span class="sxs-lookup"><span data-stu-id="efb4c-562">In practice, direct evaluation using the closed form solution is not used because it has poor numerical properties.</span></span> <span data-ttu-id="efb4c-563">Al contrario, un tipo di algoritmo di factorzzazione della matrice viene applicato alla matrice coefficiente, che riduce il sistema di equazioni a una forma canonica.</span><span class="sxs-lookup"><span data-stu-id="efb4c-563">Instead, some kind of matrix factorization algorithm is applied to the coefficient matrix which reduces the system of equations to a canonical form.</span></span> <span data-ttu-id="efb4c-564">Nell'implementazione corrente, la scomposizione di valori singolari (SVD) viene applicata alla matrice **R** e quindi il sistema decomposto risultante viene risolto.</span><span class="sxs-lookup"><span data-stu-id="efb4c-564">In the current implementation, Singular Value Decomposition (SVD) is applied to the matrix **R** and then the resulting decomposed system is solved.</span></span>

<span data-ttu-id="efb4c-565">La soluzione per il problema di regressione lineare, indicata da, ![ Mostra la soluzione al problema di regressione lineare.](images/cdmp-formula26.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-565">The solution to the linear regression problem, denoted by ![Shows the solution to the linear regression problem.](images/cdmp-formula26.png)</span></span> <span data-ttu-id="efb4c-566">, viene usato come punto iniziale dell'algoritmo Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="efb4c-566">, is used as the starting point of the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="efb4c-567">In questo algoritmo viene calcolato un passaggio di valutazione che dovrebbe spostare il punto più vicino alla soluzione ottimale.</span><span class="sxs-lookup"><span data-stu-id="efb4c-567">In this algorithm, a trial step is computed that should move the point closer to the optimal solution.</span></span> <span data-ttu-id="efb4c-568">Il passaggio di valutazione soddisfa un set di equazioni lineari che dipendono dal valore funzionale e dai valori dei derivati nel punto corrente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-568">The trial step satisfies a set of linear equations dependent on the functional value and values of the derivatives at the current point.</span></span> <span data-ttu-id="efb4c-569">Per questo motivo, i derivati della funzione Objective?</span><span class="sxs-lookup"><span data-stu-id="efb4c-569">For this reason, the derivatives of the objective function ?</span></span> <span data-ttu-id="efb4c-570">per quanto riguarda i parametri *?<sub> i</sub>*, *i <sub></sub> <sub></sub> sono gli* input obbligatori per l'algoritmo Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="efb4c-570">with respect to the parameters *?<sub>i</sub>*, *a<sub>i</sub> <sub>i</sub>* are required inputs to the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="efb4c-571">Sebbene esistano 60 parametri, è disponibile un collegamento che consente di calcolare un numero molto inferiore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-571">Although there are 60 parameters, there is a shortcut that allows you to compute a lot less.</span></span> <span data-ttu-id="efb4c-572">Dalla regola della catena di calcolo,</span><span class="sxs-lookup"><span data-stu-id="efb4c-572">By the Chain Rule of Calculus,</span></span>

![Mostra un'equazione che consente un collegamento usando la regola della catena di calcolo.](images/cdmp-formula27.png)

<span data-ttu-id="efb4c-574">dove *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub></sub>* i,*v <sub>i</sub>* è il valore CIELAB del punto di campionamento *i* , e *R <sub>IJ</sub>* è la voce *(i*,*j* ) della matrice **r** definita sopra.</span><span class="sxs-lookup"><span data-stu-id="efb4c-574">where *j* = 1, 2,  , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* are the CIELAB value of the *i* th sample point, and *R <sub>ij</sub>* is the (*i*,*j* )th entry of the matrix **R** defined above.</span></span> <span data-ttu-id="efb4c-575">Quindi, invece di calcolare i derivati per i parametri di 60, è possibile calcolare i derivati per *L*,*a* e *b* usando le differenze di avanzamento numerico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-575">So instead of computing derivatives for 60 parameters, you can compute derivatives for *L*,*a*, and *b* using numerical forward differencing.</span></span>

<span data-ttu-id="efb4c-576">È anche necessario impostare un criterio di arresto per gli algoritmi iterativi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-576">It is also necessary to set up a stopping criterion for iterative algorithms.</span></span> <span data-ttu-id="efb4c-577">Nell'implementazione corrente, le iterazioni vengono interrotte se il DECIE94 quadrato medio è minore di 1 oppure il numero di iterazioni eseguite ha superato 10.</span><span class="sxs-lookup"><span data-stu-id="efb4c-577">In the current implementation, the iterations are terminated if the mean square DECIE94 is less than 1, or the number of iterations performed has exceeded 10.</span></span> <span data-ttu-id="efb4c-578">Il numero 10 deriva dall'esperienza pratica che se le prime iterazioni non riducono significativamente l'errore, altre iterazioni non aiuteranno molto oltre lo scorrimento del punto in modo oscillante, ovvero l'algoritmo potrebbe non essere convergente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-578">The number 10 comes from the practical experience that if the first few iterations do not reduce the error significantly, further iterations would not help much other than moving the point in an oscillatory manner, i.e., the algorithm may not converge.</span></span> <span data-ttu-id="efb4c-579">Anche nel caso in cui l'algoritmo si differenzia, è possibile verificare che il DECIE94 non sia peggiore rispetto a quello iniziato, ovvero con i parametri ottenuti dalla regressione lineare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-579">Even in the case that the algorithm diverges, we can be sure that the DECIE94 is no worse than what we started, i.e. with the parameters obtained from linear regression.</span></span>

<span data-ttu-id="efb4c-580">Anche con il metodo precedente di regressione non lineare, esistono diversi problemi con l'adattamento.</span><span class="sxs-lookup"><span data-stu-id="efb4c-580">Even with the preceding method of nonlinear regression, there are several problems with the fitting.</span></span> <span data-ttu-id="efb4c-581">Un problema consiste nel fatto che i polinomi tendono a superare o sottobattere i punti dati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-581">One problem is that the polynomials tend to overshoot or undershoot beyond the data points.</span></span> <span data-ttu-id="efb4c-582">Le massime e minime locali artificiali possono essere introdotte nel processo di adattamento.</span><span class="sxs-lookup"><span data-stu-id="efb4c-582">Artificial local maxima and minima may be introduced in the fitting process.</span></span> <span data-ttu-id="efb4c-583">Questa operazione può essere neutralizzata usando polinomi di basso livello, motivo per cui non è consigliabile usare più di tre gradi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-583">This can be counteracted by using polynomials of low degree, which is the reason you should not use higher than three degrees.</span></span> <span data-ttu-id="efb4c-584">Un aspetto più grave dell'Overshooting o dell'abbattimento è che, mentre un polinomiale può assumere un valore reale teoricamente, lo spazio che tenta di modellare in genere presenta vincoli fisici e pratici.</span><span class="sxs-lookup"><span data-stu-id="efb4c-584">A more serious aspect of overshooting or undershooting is that, while a polynomial can take any real value theoretically, the space it tries to model typically has physical constraints and practical constraints.</span></span> <span data-ttu-id="efb4c-585">CIE XYZ deve avere tutti i X, Y, Z non negativi, che è un vincolo fisico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-585">CIEXYZ must have all of X, Y, Z non-negative, which is a physical constraint.</span></span> <span data-ttu-id="efb4c-586">In pratica, accettano solo valori nella grandezza di centinaia, non di migliaia o superiori.</span><span class="sxs-lookup"><span data-stu-id="efb4c-586">In practice, they only take values in the magnitude of hundreds, not thousands or higher.</span></span> <span data-ttu-id="efb4c-587">Analogamente, CIELAB o CIELUV presenta vincoli fisici e pratici.</span><span class="sxs-lookup"><span data-stu-id="efb4c-587">Similarly, CIELAB or CIELUV has its own physical and practical constraints.</span></span> <span data-ttu-id="efb4c-588">Quando lo spazio RGB viene riempito sufficientemente con i punti di campionamento, il problema dell'Overshooting o dell'overshooting non è grave.</span><span class="sxs-lookup"><span data-stu-id="efb4c-588">When the RGB space is filled sufficiently with sample points, the problem of overshooting or undershooting is not serious.</span></span> <span data-ttu-id="efb4c-589">Tuttavia, i punti RGB acquisiti dal dispositivo di acquisizione in genere non riempiono lo spazio RGB in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="efb4c-589">However, the captured RGB points from the capture device do not usually fill up the RGB space uniformly.</span></span> <span data-ttu-id="efb4c-590">I punti possono riempirsi solo interno del 80% del cubo RGB, o peggiori, possono trovarsi in un collettore di dimensioni inferiori.</span><span class="sxs-lookup"><span data-stu-id="efb4c-590">The points may fill up only inner the 80% of the RGB cube, or worse, they may reside in a lower dimensional manifold.</span></span> <span data-ttu-id="efb4c-591">Quando si verifica questo problema, i polinomi regressione possono eseguire un processo scadente per estrapolare i valori oltre i punti dati, a volte restituendo stime non realistiche.</span><span class="sxs-lookup"><span data-stu-id="efb4c-591">When this happens, the regressed polynomials may do a poor job at extrapolating the values beyond the data points, sometimes returning unrealistic predictions.</span></span> <span data-ttu-id="efb4c-592">Si desidera un modello che restituisce sempre valori ragionevolmente realistici.</span><span class="sxs-lookup"><span data-stu-id="efb4c-592">You want a model that always returns reasonably realistic values.</span></span> <span data-ttu-id="efb4c-593">Questa operazione richiede un metodo che possa controllare in modo efficace il comportamento dei limiti dei polinomi di regressione imponendo un costo aggiuntivo per i polinomi che si comportano in modo irregolare vicino al limite del cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-593">This requires a method that can effectively control the boundary behavior of regression polynomials by imposing additional cost to those polynomials that behave erratically near the boundary of the RGB cube.</span></span> <span data-ttu-id="efb4c-594">Un'ulteriore misura per assicurarsi che i polinomi restituiscano sempre i valori realistici vengono applicati ritagliando l'output all'interno del locus spettrale CIE.</span><span class="sxs-lookup"><span data-stu-id="efb4c-594">A further measure to ensure that the polynomials always return realistic values is applied by clipping the output to within the CIE spectral locus.</span></span>

<span data-ttu-id="efb4c-595">È a questo punto che la modellazione dello scanner e la modellazione della fotocamera divergeno tra loro.</span><span class="sxs-lookup"><span data-stu-id="efb4c-595">It is at this point that the scanner modeling and camera modeling diverge from each other.</span></span> <span data-ttu-id="efb4c-596">Si prevede che il modello di fotocamera venga estrapolato nelle aree oltre i punti campionati, incluse le "evidenziazioni speculari", per il modello di scanner non è necessaria la stessa estrapolazione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-596">The camera model is expected to extrapolate to regions beyond the sampled points including the "specular highlights," the same extrapolation is not required for the scanner model.</span></span> <span data-ttu-id="efb4c-597">Si prevede che la destinazione dello scanner copra una caratterizzazione simile al materiale stampato da analizzare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-597">The scanner target is expected to cover a characterization that is similar to the printed materials to be scanned.</span></span> <span data-ttu-id="efb4c-598">Il modello dello scanner è ancora necessario per essere affidabile, nel senso che non deve restituire valori non realistici, ma non è necessaria un'estrapolazione ben oltre la destinazione di caratterizzazione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-598">The scanner model is still required to be robust in the sense that it should not return unrealistic values, but extrapolation far beyond the characterization target is not required.</span></span> <span data-ttu-id="efb4c-599">Per garantire l'affidabilità, l'L-polinomiale precedente viene ritagliato a 100, ovvero il modello polinomiale è forzato a non estrapolare oltre "dmin" della destinazione dello scanner.</span><span class="sxs-lookup"><span data-stu-id="efb4c-599">To ensure robustness, the L-polynomial above is clipped at 100, that is, the polynomial model is forced not to extrapolate beyond "Dmin" of the scanner target.</span></span>

<span data-ttu-id="efb4c-600">Si prevede che il modello di fotocamera venga estrapolato in evidenza speculari, quindi il ritaglio a 100 è indesiderato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-600">The camera model is expected to extrapolate to specular highlights, so clipping at 100 is undesirable.</span></span> <span data-ttu-id="efb4c-601">Viene invece utilizzato l'algoritmo seguente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-601">Instead, the following algorithm is used.</span></span>

<span data-ttu-id="efb4c-602">I punti di controllo artificiali vengono introdotti per controllare il comportamento dei polinomi in aree con campionamento insufficiente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-602">Artificial control points are introduced to control the behavior of the polynomials in regions with insufficient sampling.</span></span> <span data-ttu-id="efb4c-603">Inserendo in modo strategico questi punti di controllo con i valori appropriati, questi vengono usati per eseguire il pull dei polinomi nella direzione richiesta.</span><span class="sxs-lookup"><span data-stu-id="efb4c-603">By strategically placing these control points with appropriate values, they serve to "pull" the polynomials in the required direction.</span></span> <span data-ttu-id="efb4c-604">Nell'implementazione corrente, vengono usati otto punti di controllo corrispondenti agli angoli del cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-604">In the current implementation, eight control points corresponding to the corners of the RGB cube are used.</span></span> <span data-ttu-id="efb4c-605">Se i valori del dispositivo vengono normalizzati in Unity, questi punti sono:</span><span class="sxs-lookup"><span data-stu-id="efb4c-605">If the device values are normalized to unity, then these points are:</span></span>

<span data-ttu-id="efb4c-606">*R* = 0, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-606">*R* = 0, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="efb4c-607">*R* = 0, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="efb4c-607">*R* = 0, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="efb4c-608">*R* = 0, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-608">*R* = 0, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="efb4c-609">*R* = 0.</span><span class="sxs-lookup"><span data-stu-id="efb4c-609">*R* = 0.</span></span> <span data-ttu-id="efb4c-610">*G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="efb4c-610">*G* = 1, *B* = 1</span></span>

<span data-ttu-id="efb4c-611">*R* = 1, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-611">*R* = 1, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="efb4c-612">*R* = 1, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="efb4c-612">*R* = 1, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="efb4c-613">*R* = 1, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="efb4c-613">*R* = 1, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="efb4c-614">*R* = 1, *G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="efb4c-614">*R* = 1, *G* = 1, *B* = 1</span></span>

<span data-ttu-id="efb4c-615">Ad eccezione del bianco *R*  = *G*  = *B* = 1, associato a un valore CIELAB di *L* = 100, *u*  = *v* = 0, viene usato l'algoritmo di estrapolazione seguente per determinare il valore CIELAB appropriato da associare a.</span><span class="sxs-lookup"><span data-stu-id="efb4c-615">Except for the white *R* =*G* =*B* = 1, which is associated with a CIELAB value of *L* = 100, *u* =*v* = 0, the following extrapolation algorithm is used to determine the appropriate CIELAB value to be associated with.</span></span> <span data-ttu-id="efb4c-616">In genere, per un determinato (*r*,*g*,*B* ), un peso è associato a ogni (*r <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) nel set di dati campionati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-616">Generally, for a given (*R*,*G*,*B* ), a weight is associated with each of the (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ) in the sampled data set.</span></span> <span data-ttu-id="efb4c-617">Esistono due obiettivi per assegnare il peso.</span><span class="sxs-lookup"><span data-stu-id="efb4c-617">There are two goals to assigning the weight.</span></span> <span data-ttu-id="efb4c-618">In primo luogo, il peso è inversamente proporzionale alla distanza tra (*r*,*g*,*b* ) e (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="efb4c-618">First, the weight is inversely proportional to the distance between (*R*,*G*,*B* ) and (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ).</span></span> <span data-ttu-id="efb4c-619">In secondo luogo, si desidera eliminare o assegnare il peso 0 a, punti con una tonalità diversa rispetto al punto specificato (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="efb4c-619">Second, you want to discard, or assign weight 0 to, points that have a different hue than the given point (*R*,*G*,*B* ).</span></span> <span data-ttu-id="efb4c-620">Per prendere in considerazione la tonalità, considerare i punti che si trovano all'interno di un cono il cui vertice si trova in (0, 0, 0), il cui asse coincide con l'Unione di riga (0, 0, 0) a (*R*,*G*,*B* ) e il cui angolo semi-verticale?</span><span class="sxs-lookup"><span data-stu-id="efb4c-620">To take the hue into account, consider points that lie within a cone whose vertex is at (0, 0, 0), whose axis coincides with the line joining (0, 0, 0) to (*R*,*G*,*B* ), and whose semi-vertical angle ?</span></span> <span data-ttu-id="efb4c-621">soddisfa i cos?</span><span class="sxs-lookup"><span data-stu-id="efb4c-621">satisfies cos ?</span></span> <span data-ttu-id="efb4c-622">= 0,9.</span><span class="sxs-lookup"><span data-stu-id="efb4c-622">= 0.9.</span></span> <span data-ttu-id="efb4c-623">Vedere la figura 3 per un'illustrazione di questo cono.</span><span class="sxs-lookup"><span data-stu-id="efb4c-623">See Figure 3 for an illustration of this cone.</span></span>

![Diagramma che mostra la forma del quartiere.](images/cdmp-lcd-dmp-figure3.png)

<span data-ttu-id="efb4c-625">**Figura 3** : filtrare i punti di esempio in base all'angolo e alla distanza.</span><span class="sxs-lookup"><span data-stu-id="efb4c-625">**Figure 3** : Filtering the sample points by angle and distance.</span></span> <span data-ttu-id="efb4c-626">La forma del quartiere raffigurato è solo a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-626">The shape of the neighborhood depicted is for illustration purpose only.</span></span> <span data-ttu-id="efb4c-627">La forma effettiva dipende dalla distanza utilizzata; si tratta di un quartiere a forma di rombo se si usa la norma 1.</span><span class="sxs-lookup"><span data-stu-id="efb4c-627">The actual shape depends on the distance used; it is a diamond-shaped neighborhood if the 1-norm is used.</span></span>

<span data-ttu-id="efb4c-628">All'interno di questo cono viene eseguito un secondo filtro basato sulla distanza RGB, che usa la norma 1, definita da</span><span class="sxs-lookup"><span data-stu-id="efb4c-628">Within this cone, a second filtering is performed that is based on the RGB distance, which uses the 1-norm, defined by</span></span>

![Mostra la formula per il secondo filtro all'interno del cono.](images/cdmp-formula28.png)

<span data-ttu-id="efb4c-630">Con il cono corrente, la ricerca iniziale è per i punti che si trovano all'interno di una distanza di 0,1 da (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="efb4c-630">With the current cone, the initial search is for points that are within a distance of 0.1 from (*R*,*G*,*B* ).</span></span> <span data-ttu-id="efb4c-631">Se non viene trovato alcun punto all'interno di questo raggio, il raggio viene aumentato di 0,1 e la ricerca viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="efb4c-631">If no point is found within this radius, the radius is increased by 0.1, and the search is restarted.</span></span> <span data-ttu-id="efb4c-632">Se le reti tonde successive non sono punti, il raggio viene aumentato di 0,1.</span><span class="sxs-lookup"><span data-stu-id="efb4c-632">If the next round nets no point either, the radius is increased by 0.1.</span></span> <span data-ttu-id="efb4c-633">Questo processo continua fino a quando il raggio supera MaxDist/5, dove MaxDist = 3, nel caso di 1-Norm.</span><span class="sxs-lookup"><span data-stu-id="efb4c-633">This process continues until the radius exceeds MaxDist/5, where MaxDist = 3, in the case of 1-norm.</span></span> <span data-ttu-id="efb4c-634">Se non viene trovato alcun punto, il cono viene ingrandito diminuendo la cos?</span><span class="sxs-lookup"><span data-stu-id="efb4c-634">If no point is found, the cone is enlarged by decreasing the cos ?</span></span> <span data-ttu-id="efb4c-635">per 0,05, ovvero l'aumento dell'angolo?</span><span class="sxs-lookup"><span data-stu-id="efb4c-635">by 0.05, that is, increasing the angle ?</span></span> <span data-ttu-id="efb4c-636">e riavviare l'intero processo con un raggio crescente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-636">and restarting the whole process with an increasing radius.</span></span> <span data-ttu-id="efb4c-637">Questo processo continua fino a quando non viene trovato un set di punti non vuoto o cos?</span><span class="sxs-lookup"><span data-stu-id="efb4c-637">This process continues until a non-empty set of points is found, or cos ?</span></span> <span data-ttu-id="efb4c-638">raggiunge 0, ovvero il cono si è aperto per diventare un piano.</span><span class="sxs-lookup"><span data-stu-id="efb4c-638">reaches 0, that is, the cone has opened up to become a plane.</span></span> <span data-ttu-id="efb4c-639">A questo punto, la ricerca viene riavviata aumentando il raggio, ad eccezione del fatto che la ricerca continua fino a quando il raggio raggiunge MaxDist.</span><span class="sxs-lookup"><span data-stu-id="efb4c-639">At this point, the search is restarted by increasing the radius, except that the search continues until the radius reaches MaxDist.</span></span> <span data-ttu-id="efb4c-640">In questo modo si garantisce che nello scenario peggiore verrà trovato un set di punti non vuoto.</span><span class="sxs-lookup"><span data-stu-id="efb4c-640">This guarantees that in the worst-case scenario, a non-empty set of points will be found.</span></span> <span data-ttu-id="efb4c-641">L'algoritmo viene riepilogato nel diagramma di flusso della figura 4.</span><span class="sxs-lookup"><span data-stu-id="efb4c-641">The algorithm is summarized in the flow diagram in Figure 4.</span></span>

![Diagramma che mostra il flusso dell'algoritmo.](images/cdmp-lcd-dmp-figure4.png)

<span data-ttu-id="efb4c-643">**Figura 4** : diagramma di flusso per determinare il set di punti di esempio usati nell'estrapolazione per un valore RGB di input</span><span class="sxs-lookup"><span data-stu-id="efb4c-643">**Figure 4** : Flow diagram for determining the set S of sample points used in the extrapolation for an input RGB value</span></span>

<span data-ttu-id="efb4c-644">Supponendo che il processo precedente restituisca *un set di* punti non vuoto (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ) e corrispondente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), quindi per ogni punto, viene assegnato un peso *w <sub>i</sub>* , fornito da</span><span class="sxs-lookup"><span data-stu-id="efb4c-644">Assuming that the preceding process yields a non-empty set *S* of points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) and corresponding (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), then for each such point, a weight *w<sub>i</sub>* is assigned, given by</span></span>

![Mostra la formula per un peso per ogni punto.](images/cdmp-formula29.png)

<span data-ttu-id="efb4c-646">Infine, extrapolant è definito da</span><span class="sxs-lookup"><span data-stu-id="efb4c-646">Finally, the extrapolant is defined by</span></span>

![Mostra la definizione di extrapolant.](images/cdmp-formula30.png)

<span data-ttu-id="efb4c-648">Le equazioni precedenti costituiscono un'istanza dei "Metodi ponderati per la distanza inversa", comunemente detti metodi Shepard.</span><span class="sxs-lookup"><span data-stu-id="efb4c-648">The preceding equations constitute an instance of the "inverse-distance weighted methods," commonly called the Shepard methods.</span></span> <span data-ttu-id="efb4c-649">Eseguendo ognuno degli otto punti da EQ (6) attraverso l'algoritmo, vengono ottenuti otto punti di controllo, ognuno con i valori *R*,*G*,*B* e *L*,*a*,*b* , che vengono inseriti nel pool con i dati di esempio originali.</span><span class="sxs-lookup"><span data-stu-id="efb4c-649">By running each of the eight points from eq (6) through the algorithm, eight control points are obtained, each with *R*,*G*,*B* and *L*,*a*,*b* values, which are put into the pool with the original sample data.</span></span>

<span data-ttu-id="efb4c-650">Per assicurarsi che il modello produca sempre valori di colore validi e per l'integrità del sistema e la stabilità dell'intera pipeline di elaborazione dei colori, è necessario eseguire un ritaglio finale all'output del modello polinomiale.</span><span class="sxs-lookup"><span data-stu-id="efb4c-650">To ensure that the model always produces valid color values and for system integrity and stability down the whole color processing pipeline, you must perform a final clipping to the output of the polynomial model.</span></span> <span data-ttu-id="efb4c-651">La gamma di oggetti visivi CIE è descritta dal componente acromatico (*Y* o *L* ) e dal componente cromatico (*XY* o *a'b '*, correlati allo spazio XYZ da una trasformazione proiettiva).</span><span class="sxs-lookup"><span data-stu-id="efb4c-651">The CIE visual gamut is described by the achromatic component (*Y* or *L* ) and the chromatic component (*xy* or *a'b'*, which are related to the XYZ space by a projective transformation).</span></span> <span data-ttu-id="efb4c-652">Nell'implementazione corrente viene usata la cromaticità *a'b* , in quanto è direttamente correlata allo spazio CIELUV.</span><span class="sxs-lookup"><span data-stu-id="efb4c-652">In the current implementation, the *a'b'* chromaticity is used because it is directly related to the CIELUV space.</span></span> <span data-ttu-id="efb4c-653">Per qualsiasi valore *CIELAB* , prima ritagliare *L* su un valore non negativo:</span><span class="sxs-lookup"><span data-stu-id="efb4c-653">For any *CIELAB* value, first clip *L* to a non-negative value:</span></span>

![Mostra il ritaglio di L a un valore non negativo.](images/cdmp-formula31.png)

<span data-ttu-id="efb4c-655">Per consentire l'estrapolazione per le evidenziazioni speculari, *L* non viene ritagliato a 100, il limite superiore "convenzionale" per *l* nello spazio Lab.</span><span class="sxs-lookup"><span data-stu-id="efb4c-655">To allow extrapolation for specular highlights, *L* is not clipped at 100, the "conventional" upper bound for *L* in Lab space.</span></span>

<span data-ttu-id="efb4c-656">Successivamente, se *L* = 0, *a* e *b* vengono ritagliati in modo che a *= b =* 0.</span><span class="sxs-lookup"><span data-stu-id="efb4c-656">Next, if *L* = 0, then *a* and *b* are clipped such that a *= b =* 0.</span></span> <span data-ttu-id="efb4c-657">Se *L* ?</span><span class="sxs-lookup"><span data-stu-id="efb4c-657">If *L* ?</span></span> <span data-ttu-id="efb4c-658">0, calcola</span><span class="sxs-lookup"><span data-stu-id="efb4c-658">0, calculate</span></span>

![Mostra la formula se L = 0.](images/cdmp-formula32.png)

<span data-ttu-id="efb4c-660">Questi sono i componenti di un vettore nel diagramma *a'b* dal punto bianco (*u?'*,*v?'*</span><span class="sxs-lookup"><span data-stu-id="efb4c-660">These are the components of a vector in the *a'b'* diagram from the white point (*u?'*,*v?'*</span></span> <span data-ttu-id="efb4c-661">) per il colore in questione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-661">) to the color in question.</span></span> <span data-ttu-id="efb4c-662">Definire il locus spettrale CIE come struttura convessa di tutti i punti (*a'*,*b '* ) con parametri per la lunghezza?:</span><span class="sxs-lookup"><span data-stu-id="efb4c-662">Define the CIE spectral locus as the convex hull of all the points (*a'*,*b'* ), parameterized by the wavelength ?:</span></span>

![Mostra la formula per la lunghezza.](images/cdmp-formula33.png)

<span data-ttu-id="efb4c-664">dove ![ Mostra le funzioni per la corrispondenza dei colori CIE.](images/cdmp-formula34.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-664">where ![Shows the functions for CIE color-matching.](images/cdmp-formula34.png)</span></span> <span data-ttu-id="efb4c-665">sono le funzioni di corrispondenza dei colori CIE per l'osservatore di 2 gradi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-665">are the CIE color-matching functions for the 2-degree observer.</span></span> <span data-ttu-id="efb4c-666">Se il vettore si trova al di fuori del locus CIE, il colore viene ritagliato fino al punto nel locus CIE che rappresenta l'intersezione tra il locus e la riga definita dal vettore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-666">If the vector lies outside the CIE locus, the color is clipped to the point on the CIE locus that is the intersection of the locus and the line defined by the vector.</span></span> <span data-ttu-id="efb4c-667">Vedere Figura 5.</span><span class="sxs-lookup"><span data-stu-id="efb4c-667">See Figure 5.</span></span> <span data-ttu-id="efb4c-668">Se si è verificato il ritaglio, il valore *a* e *b* viene ricostruito prima sottraendo *un?'*</span><span class="sxs-lookup"><span data-stu-id="efb4c-668">If clipping has occurred, the *a* and *b* value is reconstructed by first subtracting *a?'*</span></span> <span data-ttu-id="efb4c-669">e *b? "*</span><span class="sxs-lookup"><span data-stu-id="efb4c-669">and *b?'*</span></span> <span data-ttu-id="efb4c-670">dal troncato *a "* e *b"*, quindi moltiplicando per 13 *L*.</span><span class="sxs-lookup"><span data-stu-id="efb4c-670">from the clipped *a'* and *b'*, and then multiplying by 13 *L*.</span></span>

![Diagramma che mostra il grafico per l'algoritmo di ritaglio.](images/cdmp-lcd-dmp-figure5.png)

<span data-ttu-id="efb4c-672">**Figura 5** : algoritmo di ritaglio per i valori Lab esterni al gamut visivo Cie</span><span class="sxs-lookup"><span data-stu-id="efb4c-672">**Figure 5** : Clipping algorithm for Lab values that are outside the CIE visual gamut</span></span>

<span data-ttu-id="efb4c-673">Nell'implementazione corrente, il locus spettrale CIE nel piano *a'b* è rappresentato da una curva lineare a tratti con segmenti 35 (corrispondenti a una lunghezza compresa tra 360 e 700 nm).</span><span class="sxs-lookup"><span data-stu-id="efb4c-673">In the current implementation, the CIE spectral locus in the *a'b'* plane is represented by a piecewise linear curve with 35 segments (corresponding to a wavelength from 360 nm to 700 nm inclusive).</span></span> <span data-ttu-id="efb4c-674">Ordinando i segmenti di linea in modo che i rispettivi angoli in base al punto bianco siano in ordine crescente, che equivale a lunghezze d'onda decrescenti, il segmento di linea che si interseca con il raggio formato dal vettore sopra riportato può essere trovato da una semplice ricerca binaria.</span><span class="sxs-lookup"><span data-stu-id="efb4c-674">By ordering the line segments so that their subtended angles at the white point are ascending, which is equivalent to descending wavelengths, the line segment that intersects with the ray formed by the above vector can be found by a simple binary search.</span></span>

### <a name="rgb-printer-device-model-baseline"></a><span data-ttu-id="efb4c-675">Baseline modello dispositivo stampante RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-675">RGB Printer Device Model Baseline</span></span>

<span data-ttu-id="efb4c-676">Una descrizione del dispositivo di una stampante RGB è costituita dalla creazione di un modello empirico del dispositivo che prevede il colore CIELUV indipendente dal dispositivo per qualsiasi valore RGB specificato</span><span class="sxs-lookup"><span data-stu-id="efb4c-676">A device characterization of a RGB printer consists of constructing an empirical model of the device that predicts the device-independent CIELUV color for any given RGB value</span></span>

<span data-ttu-id="efb4c-677">Esistono due modi per costruire il modello empirico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-677">There are two ways to construct the empirical model.</span></span> <span data-ttu-id="efb4c-678">Un modo consiste nell'usare i dati del dispositivo per una stampante RGB e l'altro per usare i dati dei parametri analitici.</span><span class="sxs-lookup"><span data-stu-id="efb4c-678">One way is to use the device data for a RGB printer, and the other is to use analytical parameter data.</span></span> <span data-ttu-id="efb4c-679">Nel primo, i dati di misurazione forniti da un utente per un dispositivo di stampa RGB vengono usati per creare la tabella di ricerca 3D (LUT).</span><span class="sxs-lookup"><span data-stu-id="efb4c-679">In the first one, measurement data provided by a user for a RGB printer device is used to construct 3-D lookup table (LUT).</span></span> <span data-ttu-id="efb4c-680">I dati di misurazione sono costituiti da valori XYZ per le patch RGB campionate in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="efb4c-680">The measurement data consists of XYZ values for uniformly sampled RGB patches.</span></span> <span data-ttu-id="efb4c-681">Le dimensioni di campionamento tipiche sono 9 o 17 per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-681">Typical sampling sizes are 9 or 17 for each component.</span></span> <span data-ttu-id="efb4c-682">Ogni patch viene misurata con un colorimetro o uno spettrofotometro nello spazio CIE XYZ.</span><span class="sxs-lookup"><span data-stu-id="efb4c-682">Each patch is measured with a colorimeter or spectrophotometer in CIEXYZ space.</span></span> <span data-ttu-id="efb4c-683">Il valore XYZ per una patch viene quindi convertito in valore CIELUV, formando un LUT 3D.</span><span class="sxs-lookup"><span data-stu-id="efb4c-683">The XYZ value for a patch is then converted into CIELUV value, forming a 3-D LUT.</span></span> <span data-ttu-id="efb4c-684">Nel modello di dispositivo, il metodo di interpolazione tetraedrica di Sakamoto viene applicato al LUT 3D per stimare i dati CIELUV per i dati RGB specificati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-684">In the device model, the Sakamoto's tetrahedral interpolation method is applied to the 3-D LUT in order to predict the CIELUV data for a given RGB data.</span></span> <span data-ttu-id="efb4c-685">(Conferisce il brevetto US 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="efb4c-685">(Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="efb4c-686">I due brevetti citati sono scaduti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-686">The two patents mentioned have expired.).</span></span> <span data-ttu-id="efb4c-687">I dati dei parametri analitici passati nel secondo metodo sono semplicemente un LUT compilato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="efb4c-687">The analytical parameter data passed in the second method is simply a LUT that was built previously.</span></span> <span data-ttu-id="efb4c-688">In genere, LUT è stato creato usando il primo metodo, sebbene possa essere creato manualmente.</span><span class="sxs-lookup"><span data-stu-id="efb4c-688">Typically, that LUT was built using the first method, although it could be hand-built.</span></span>

<span data-ttu-id="efb4c-689">Nella gestione dei colori corrente la mappa di origine è definita come mappa che passa dallo spazio RGB a uno spazio di colore CIE XYZ indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-689">In the current color management, the source map is defined as the map that goes from RGB space to a device-independent CIEXYZ color space.</span></span> <span data-ttu-id="efb4c-690">La mappa di destinazione viene definita come mappa che passa dallo spazio di colore CIE XYZ indipendente dal dispositivo allo spazio RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-690">The destination map is defined as the map that goes from the device-independent CIEXYZ color space to RGB space.</span></span> <span data-ttu-id="efb4c-691">Si tratta dell'inverso della mappa di origine.</span><span class="sxs-lookup"><span data-stu-id="efb4c-691">It is the inverse of the source map.</span></span>

<span data-ttu-id="efb4c-692">Il modello empirico viene usato direttamente nella mappa di origine.</span><span class="sxs-lookup"><span data-stu-id="efb4c-692">The empirical model is directly used in the source map.</span></span> <span data-ttu-id="efb4c-693">Esegue prima il mapping di un dato RGB dati in un CIELUV dati, che viene convertito in dati XYZ.</span><span class="sxs-lookup"><span data-stu-id="efb4c-693">It first maps a given RGB data into a CIELUV data, which is converted into XYZ data.</span></span> <span data-ttu-id="efb4c-694">Nella mappa di destinazione i dati CIE XYZ indipendenti dal dispositivo vengono prima convertiti in dati di CIELUV.</span><span class="sxs-lookup"><span data-stu-id="efb4c-694">In the destination map, device-independent CIEXYZ data is first converted into CIELUV data.</span></span> <span data-ttu-id="efb4c-695">Quindi, il modello empirico e il metodo di Newton-Raphson classico vengono usati per stimare i dati RGB migliori per i dati CIELUV.</span><span class="sxs-lookup"><span data-stu-id="efb4c-695">Then, the empirical model and the classical Newton-Raphson method are used to predict the best RGB data for the CIELUV data.</span></span> <span data-ttu-id="efb4c-696">I dettagli sulla conversione da CieLUV a dati RGB sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="efb4c-696">The details about conversion from CieLUV to RGB data are as follows:</span></span>

<span data-ttu-id="efb4c-697">Dopo la generazione di un LUT 3D da RGB a CieLUV, la mappa da RGB a LUV viene compilata usando l'interpolazione tetraedrica su RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-697">After generating a 3-D LUT from RGB to CieLUV, the map from RGB to LUV is built using tetrahedral interpolation on RGB.</span></span> <span data-ttu-id="efb4c-698">Questa mappa è indicata dalle equazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="efb4c-698">This map is denoted by the following equations:</span></span>

![Mostra le equazioni per la mappa da R G B a L U V.](images/cdmp-image125.png)

<span data-ttu-id="efb4c-700">L'inversione della mappa è costituita dalla risoluzione, per qualsiasi colore</span><span class="sxs-lookup"><span data-stu-id="efb4c-700">Inversion of the map consists of solving, for any color</span></span> ![Mostra L U V.](images/cdmp-image127.png) <span data-ttu-id="efb4c-702">, il sistema seguente di equazioni non lineari:</span><span class="sxs-lookup"><span data-stu-id="efb4c-702">, the following system of nonlinear equations:</span></span>

![Mostra le equazioni non lineari per lolving qualsiasi colore L U V.](images/cdmp-image129.png)

<span data-ttu-id="efb4c-704">Nella nuova CTE viene utilizzata un'equazione non lineare basata sul metodo di Newton-Raphson classico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-704">A nonlinear equation that is based on the classical Newton-Raphson method is used in the new CTE.</span></span> <span data-ttu-id="efb4c-705">Una supposizione iniziale, o *una precedente* , <sub>prima</sub> di, (R 0, G 0, B 0) viene ottenuta tramite la ricerca di una "matrice di inizializzazione" costituita da una griglia 8x8x8 uniforme di coppie pre-calcolate (RGB, Luv).</span><span class="sxs-lookup"><span data-stu-id="efb4c-705">An initial guess, or *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) is obtained by searching through a "seed matrix" consisting of a uniform 8x8x8 grid of pre-computed (RGB,Luv) pairs.</span></span> <span data-ttu-id="efb4c-706">Viene scelto il Luv corrispondente di RGB più vicino a L \* u \* v \* .</span><span class="sxs-lookup"><span data-stu-id="efb4c-706">The RGB corresponding Luv that is closest to the L\*u\*v\* is chosen.</span></span> <span data-ttu-id="efb4c-707">Ogni punto della matrice di inizializzazione corrisponde al centro di una cella in modo che le iterazioni non inizino con un punto sulla faccia limite del cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-707">Each point in the seed matrix corresponds to the center of a cell so that the iterations don't start with a point on the boundary face of the RGB cube.</span></span> <span data-ttu-id="efb4c-708">In altre parole, l'RGB dei semi viene definito da: STEP = 1/8 s <sub>IJK</sub> = (Step/2 + (i-1) Step, Step/2 + (j-1) STEP, Step/2 + (k-1) Step) with i, j, k = 1... 8 nel passaggio *i* ° di Newton-Raphson, la stima successiva ![ Mostra le variabili per la stima successiva.](images/cdmp-image133.png)</span><span class="sxs-lookup"><span data-stu-id="efb4c-708">In other words, the RGB of the seeds is defined by: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At the *i* th step of Newton-Raphson, the next estimate ![Shows the variables for the next estimate.](images/cdmp-image133.png)</span></span> <span data-ttu-id="efb4c-709">viene ottenuto dalla formula:</span><span class="sxs-lookup"><span data-stu-id="efb4c-709">is obtained by the formula:</span></span>

![Mostra la formula per la stima.](images/cdmp-image135.png)

<span data-ttu-id="efb4c-711">L'iterazione si interrompe quando l'errore (distanza nello spazio CIELUV) è inferiore a un livello di tolleranza preimpostato (0,1 nella CTE) o quando il numero di iterazioni ha superato il numero massimo consentito di iterazioni (10 nella CTE).</span><span class="sxs-lookup"><span data-stu-id="efb4c-711">Iteration stops when the error (distance in the CIELUV space) is less than a pre-set tolerance level (0.1 in the CTE), or when the number of iterations has exceeded the maximum allowed number of iterations (10 in the CTE).</span></span> <span data-ttu-id="efb4c-712">I valori per la tolleranza e il numero di iterazioni sono stati determinati in modo empirico come validi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-712">The values for the tolerance and the number of iterations were empirically determined to be effective.</span></span> <span data-ttu-id="efb4c-713">Nelle versioni future, il valore di tolleranza può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-713">In future versions, the tolerance value may be changed.</span></span>

<span data-ttu-id="efb4c-714">La matrice jacobiano viene calcolata usando la differenza in avanti, tranne che in corrispondenza di un punto limite (uno o più dei R, G, B è 1) in cui viene invece usata la differenza tra le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-714">The Jacobian matrix is calculated using forward difference, except at a boundary point (one or more of the R, G, B is 1) where backward difference is used instead.</span></span> <span data-ttu-id="efb4c-715">Invece di calcolare l'inverso della matrice jacobiano, il sistema lineare viene risolto direttamente usando Gauss-Jordan l'eliminazione con l'intera trasformazione pivot.</span><span class="sxs-lookup"><span data-stu-id="efb4c-715">Instead of calculating the inverse of the Jacobian matrix, the linear system is solved directly using Gauss-Jordan elimination with full pivoting.</span></span>

<span data-ttu-id="efb4c-716">Alla fine delle iterazioni, è possibile che la convergenza non venga comunque eseguita perché Newton-Raphson è un algoritmo "locale", ovvero funziona correttamente se si inizia con una supposizione iniziale vicina alla soluzione vera e propria.</span><span class="sxs-lookup"><span data-stu-id="efb4c-716">At the end of the iterations, convergence still might not be achieved because Newton-Raphson is a "local" algorithm, that is, it only works well if you start with an initial guess that is close to the true solution.</span></span> <span data-ttu-id="efb4c-717">Se, alla fine del Newton-Raphson iterazioni, la convergenza entro la tolleranza di errore predefinita non è stata realizzata, le iterazioni vengono riavviate con un nuovo set di semi, definito come segue.</span><span class="sxs-lookup"><span data-stu-id="efb4c-717">If, at the end of the Newton-Raphson iterations, convergence within the pre-defined error tolerance has not been achieved, the iterations are restarted with a new set of seeds, defined as follows.</span></span>

<span data-ttu-id="efb4c-718">Ad esempio, la soluzione migliore ottenuta finora è (r, g, b).</span><span class="sxs-lookup"><span data-stu-id="efb4c-718">For example, the best solution obtained so far is (r, g, b).</span></span> <span data-ttu-id="efb4c-719">Da questa soluzione vengono derivati i semi a posteriori, dove N = 4.</span><span class="sxs-lookup"><span data-stu-id="efb4c-719">From this solution, N a posteriori seeds are derived, where N = 4.</span></span> <span data-ttu-id="efb4c-720">In modo intuitivo, la soluzione viene spostata "verso il centro" in una dimensione del passaggio che dipende da N. Vedere la figura 6.</span><span class="sxs-lookup"><span data-stu-id="efb4c-720">Intuitively, the solution is moved "toward the center" in a step size that depends on N. See Figure 6.</span></span>

![Diagramma che mostra le direzioni di perturbazione della soluzione.](images/cdmp-image136.png)

<span data-ttu-id="efb4c-722">**Figura 6** : la direzione di perturbazione della soluzione dipende da quale ottetto si trova in.</span><span class="sxs-lookup"><span data-stu-id="efb4c-722">**Figure 6** : Perturbation direction of the solution depends on which octant it is in.</span></span>

<span data-ttu-id="efb4c-723">In altre parole, se r &gt; 0,5, il valore sul canale r viene ridotto; in caso contrario, il valore viene aumentato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-723">In other words, if r &gt; 0.5, the value on the R channel is decreased, otherwise the value is increased.</span></span> <span data-ttu-id="efb4c-724">Esiste una logica simile per i canali G e B.</span><span class="sxs-lookup"><span data-stu-id="efb4c-724">There is similar logic for the G and B channels.</span></span> <span data-ttu-id="efb4c-725">Le definizioni esatte sono:</span><span class="sxs-lookup"><span data-stu-id="efb4c-725">The precise definitions are:</span></span>

<span data-ttu-id="efb4c-726">PERTURBATION = 0,5/(N + 1)</span><span class="sxs-lookup"><span data-stu-id="efb4c-726">PERTURBATION = 0.5/(N+1)</span></span>

<span data-ttu-id="efb4c-727">Dir (r) =-1 se r &gt; 0,5; + 1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="efb4c-727">Dir(r) = -1 if r &gt; 0.5; +1 otherwise.</span></span> <span data-ttu-id="efb4c-728">In modo analogo per dir (g) e dir (b)</span><span class="sxs-lookup"><span data-stu-id="efb4c-728">Similarly for Dir(g) and Dir(b)</span></span>

<span data-ttu-id="efb4c-729">Il valore di inizializzazione di JTH a posteriori, s????, è (r + dir (r) j Perturbation \* \* , g + dir (g) j Perturbation \* \* , b + dir (b) \* j \* Perturbation)</span><span class="sxs-lookup"><span data-stu-id="efb4c-729">The jth a posteriori seed, s ????, is (r + Dir(r) \*j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)</span></span>

<span data-ttu-id="efb4c-730">Prova la prima s????</span><span class="sxs-lookup"><span data-stu-id="efb4c-730">Try the first s ????</span></span> <span data-ttu-id="efb4c-731">e se fornisce una nuova soluzione entro la tolleranza di errore, è possibile arrestare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-731">and if it gives a new solution within error tolerance, you can stop.</span></span> <span data-ttu-id="efb4c-732">In caso contrario, provare la seconda s????</span><span class="sxs-lookup"><span data-stu-id="efb4c-732">Otherwise, try the second s ????</span></span> <span data-ttu-id="efb4c-733">e così via fino all'ennesimo????.</span><span class="sxs-lookup"><span data-stu-id="efb4c-733">and so on until the Nth s ????.</span></span>

<span data-ttu-id="efb4c-734">Le schematiche dell'intero algoritmo sono illustrate nella figura 7.</span><span class="sxs-lookup"><span data-stu-id="efb4c-734">The schematics of the whole algorithm is shown in Figure 7.</span></span>

![Diagramma che mostra il flusso per l'inversione del modello di dispositivo.](images/cdmp-image138.png)

<span data-ttu-id="efb4c-736">**Figura 7** : schemi di inversione del modello di dispositivo</span><span class="sxs-lookup"><span data-stu-id="efb4c-736">**Figure 7** : Schematics of inverting the device model</span></span>

### <a name="rgb-virtual-device-model-baseline"></a><span data-ttu-id="efb4c-737">Linea di base del modello di dispositivo virtuale RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-737">RGB Virtual Device Model Baseline</span></span>

<span data-ttu-id="efb4c-738">Questo modello di dispositivo (DM) è un semplice algoritmo di riproduzione a matrice/tono.</span><span class="sxs-lookup"><span data-stu-id="efb4c-738">This device model(DM) is a simple matrix/tone reproduction algorithm.</span></span> <span data-ttu-id="efb4c-739">La matrice viene derivata dal punto bianco e dalle primarie usando gli algoritmi di scienza dei colori standard.</span><span class="sxs-lookup"><span data-stu-id="efb4c-739">The matrix is derived from the white point and primaries using standard color science algorithms.</span></span> <span data-ttu-id="efb4c-740">La curva di riproduzione del tono è derivata dai parametri di misurazione in base alle descrizioni ICC di CurveType e ParametricType (o invertite in base alle esigenze).</span><span class="sxs-lookup"><span data-stu-id="efb4c-740">The tone reproduction curve is derived from the measurement parameters according to the ICC descriptions of CurveType and ParametricType (or inverted as required).</span></span> <span data-ttu-id="efb4c-741">I dettagli degli algoritmi interni verranno forniti dopo la convalida aggiuntiva di problemi di intervallo dinamico elevato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-741">Details of the internal algorithms will be provided after additional validation of high dynamic range issues.</span></span>

<span data-ttu-id="efb4c-742">Il modello di dispositivo virtuale RGB è una curva di riproduzione a matrice/tono idealizzata RGB simile alla progettazione del profilo basato su matrice di tre componenti di ICC.</span><span class="sxs-lookup"><span data-stu-id="efb4c-742">The RGB virtual device model is an idealized matrix/tone reproduction curve RGB similar to the ICC three-component matrix-based profile design.</span></span> <span data-ttu-id="efb4c-743">I parametri di "misurazione virtuale" del DM includono un valore di punto bianco (CIE XYZ assoluto), i valori primari RGB (CIE XYZ assoluti) e una curva di riproduzione del tono basata sulle ParametricCurveType ICC e CurveType in formato XML coerenti con gli schemi DMP.</span><span class="sxs-lookup"><span data-stu-id="efb4c-743">The "virtual measurement" parameters of the DM include a white point value (absolute CIEXYZ), RGB primary values (absolute CIEXYZ), and a tone reproduction curve that is based on the ICC ParametricCurveType and CurveType in XML formatting consistent with the DMP schemas.</span></span>

<span data-ttu-id="efb4c-744">La tabella seguente illustra la codifica del tipo di funzione ICC parametricCurveType e il supporto corrispondente in IRGBVirtualDeviceModelBase.</span><span class="sxs-lookup"><span data-stu-id="efb4c-744">ICC parametricCurveType function type encoding and corresponding support in IRGBVirtualDeviceModelBase are shown in the following table.</span></span>



| <span data-ttu-id="efb4c-745">Tipo di funzione</span><span class="sxs-lookup"><span data-stu-id="efb4c-745">Function type</span></span>                                         | <span data-ttu-id="efb4c-746">Parametri</span><span class="sxs-lookup"><span data-stu-id="efb4c-746">Parameters</span></span>                          | <span data-ttu-id="efb4c-747">Tipo</span><span class="sxs-lookup"><span data-stu-id="efb4c-747">Type</span></span>                                     | <span data-ttu-id="efb4c-748">Nota</span><span class="sxs-lookup"><span data-stu-id="efb4c-748">Note</span></span>                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Mostra la funzione ' GammaType '.](images/cdmp-image154.png)<br/> | <span data-ttu-id="efb4c-750">g</span><span class="sxs-lookup"><span data-stu-id="efb4c-750">g</span></span><br/>              | <span data-ttu-id="efb4c-751">GammaType</span><span class="sxs-lookup"><span data-stu-id="efb4c-751">GammaType</span></span><br/>                 | <span data-ttu-id="efb4c-752">Implementazione comune</span><span class="sxs-lookup"><span data-stu-id="efb4c-752">Common implementation</span></span><br/>           |
| ![Mostra la funzione ' GammaOffsetGainType '.](images/cdmp-image156.png)<br/> | <span data-ttu-id="efb4c-754">GA b</span><span class="sxs-lookup"><span data-stu-id="efb4c-754">ga b</span></span><br/>           | <span data-ttu-id="efb4c-755">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="efb4c-755">GammaOffsetGainType</span></span><br/>       | <span data-ttu-id="efb4c-756">CIE 122-1966</span><span class="sxs-lookup"><span data-stu-id="efb4c-756">CIE 122-1966</span></span><br/>                    |
| ![Mostra la funzione ' GammaOffsetGainOffsetType '.](images/cdmp-image158.png)<br/> | <span data-ttu-id="efb4c-758">GA b c</span><span class="sxs-lookup"><span data-stu-id="efb4c-758">ga b c</span></span><br/>         | <span data-ttu-id="efb4c-759">GammaOffsetGainOffsetType</span><span class="sxs-lookup"><span data-stu-id="efb4c-759">GammaOffsetGainOffsetType</span></span><br/> | <span data-ttu-id="efb4c-760">IEC 61966-3</span><span class="sxs-lookup"><span data-stu-id="efb4c-760">IEC 61966-3</span></span><br/>                     |
| ![Mostra la funzione ' GammaOffsetGainGainType '.](images/cdmp-image160.png)<br/> | <span data-ttu-id="efb4c-762">GA b c d</span><span class="sxs-lookup"><span data-stu-id="efb4c-762">ga b c d</span></span><br/>       | <span data-ttu-id="efb4c-763">GammaOffsetGainGainType</span><span class="sxs-lookup"><span data-stu-id="efb4c-763">GammaOffsetGainGainType</span></span><br/>   | <span data-ttu-id="efb4c-764">IEC 61966-2.1</span><span class="sxs-lookup"><span data-stu-id="efb4c-764">IEC 61966-2.1</span></span><br/> <span data-ttu-id="efb4c-765">sRGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-765">(sRGB)</span></span><br/> |
| ![Mostra una funzione per i parametri ' g a b c d e f '.](images/cdmp-image162.png)<br/> | <span data-ttu-id="efb4c-767">GA b c d e f</span><span class="sxs-lookup"><span data-stu-id="efb4c-767">ga b c d e f</span></span><br/>   | <span data-ttu-id="efb4c-768">N/D</span><span class="sxs-lookup"><span data-stu-id="efb4c-768">N/A</span></span><br/>                       | <span data-ttu-id="efb4c-769">Non supportato in WCS</span><span class="sxs-lookup"><span data-stu-id="efb4c-769">Not supported in WCS</span></span><br/>            |



 

<span data-ttu-id="efb4c-770">La curva di tono per i dispositivi virtuali RGB viene applicata in DeviceToColorimetric tra i dati di input, pDeviceColors e la moltiplicazione della matrice.</span><span class="sxs-lookup"><span data-stu-id="efb4c-770">The tone curve for RGB virtual devices is applied in DeviceToColorimetric between the input data, pDeviceColors, and the matrix multiply.</span></span> <span data-ttu-id="efb4c-771">Per ColorimetricToDevice, è necessario usare un metodo per invertire la curva di tono.</span><span class="sxs-lookup"><span data-stu-id="efb4c-771">For ColorimetricToDevice, a method must be used to invert the tone curve.</span></span> <span data-ttu-id="efb4c-772">Nell'implementazione di base questa operazione viene eseguita dall'interpolazione diretta nella stessa curva di tono utilizzata per DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="efb4c-772">In the baseline implementation, this is done by direct interpolation in the same tone curve used for DeviceToColorimetric.</span></span>

<span data-ttu-id="efb4c-773">Le curve devono essere specificate nei profili come coppie di numeri nello spazio float.</span><span class="sxs-lookup"><span data-stu-id="efb4c-773">The curves should be specified in the profiles as pairs of numbers in float space.</span></span> <span data-ttu-id="efb4c-774">Il primo numero rappresenta i valori in pDeviceColors.</span><span class="sxs-lookup"><span data-stu-id="efb4c-774">The first number represents values in pDeviceColors.</span></span> <span data-ttu-id="efb4c-775">Il secondo numero rappresenta l'output della curva di tono.</span><span class="sxs-lookup"><span data-stu-id="efb4c-775">The second number represents the output of the tone curve.</span></span> <span data-ttu-id="efb4c-776">Tutti i valori nella curva di tono devono essere compresi tra minColorantUsed e maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="efb4c-776">All values in the tone curve must be between minColorantUsed and maxColorantUsed.</span></span> <span data-ttu-id="efb4c-777">Le curve di tono devono contenere almeno due voci, una per minColorantUsed e una per maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="efb4c-777">Tone curves must contain at least two entries: one for minColorantUsed and one for maxColorantUsed.</span></span> <span data-ttu-id="efb4c-778">Il numero massimo di voci in ToneCurve è 2048.</span><span class="sxs-lookup"><span data-stu-id="efb4c-778">The maximum number of entries in the ToneCurve is 2048.</span></span> <span data-ttu-id="efb4c-779">In generale, maggiore è il numero di voci nella tabella, più accuratamente è possibile modellare la curvatura.</span><span class="sxs-lookup"><span data-stu-id="efb4c-779">In general, the more entries in the table, the more accurately you can model curvature.</span></span> <span data-ttu-id="efb4c-780">Viene eseguita un'interpolazione lineare a tratti tra le voci.</span><span class="sxs-lookup"><span data-stu-id="efb4c-780">A piecewise linear interpolation is performed between the entries.</span></span>

<span data-ttu-id="efb4c-781">È possibile considerare metodi di interpolazione alternativi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-781">You might consider alternative interpolation methods.</span></span> <span data-ttu-id="efb4c-782">Se si conosce qualcosa sul comportamento sottostante del dispositivo, è possibile usare un minor numero di campioni e un modello più accurato con una curva di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-782">If you know something about the underlying behavior of the device, you can use fewer samples and model more accurately with a higher order curve.</span></span> <span data-ttu-id="efb4c-783">Tuttavia, se si usa il tipo di curva errato, sarà molto impreciso.</span><span class="sxs-lookup"><span data-stu-id="efb4c-783">But if you use the wrong curve type, you will be very inaccurate.</span></span> <span data-ttu-id="efb4c-784">Senza ulteriori informazioni, non è possibile indovinare il tipo di curva.</span><span class="sxs-lookup"><span data-stu-id="efb4c-784">Without more information, you cannot guess the curve type.</span></span> <span data-ttu-id="efb4c-785">Quindi, usare l'interpolazione lineare e fornire molti punti dati.</span><span class="sxs-lookup"><span data-stu-id="efb4c-785">So, use linear interpolation and provide many data points.</span></span>

### <a name="cmyk-printer-device-model-baseline"></a><span data-ttu-id="efb4c-786">Baseline modello di dispositivo stampante CMYK</span><span class="sxs-lookup"><span data-stu-id="efb4c-786">CMYK Printer Device Model Baseline</span></span>

<span data-ttu-id="efb4c-787">Una descrizione del dispositivo di una stampante CMYK è costituita dalla creazione di un modello empirico del dispositivo che prevede il colore stampato per un determinato valore CMYK.</span><span class="sxs-lookup"><span data-stu-id="efb4c-787">A device characterization of a CMYK printer consists of constructing an empirical model of the device that predicts the printed color for any given CMYK value.</span></span> <span data-ttu-id="efb4c-788">La caratterizzazione include anche l'inversione di questo modello, in modo che sia possibile assegnare una prescrizione del valore CMYK a noi per un determinato colore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-788">The characterization also includes the inversion of this model so that a prescription of the CMYK value to us for a given color to be printed can be given.</span></span> <span data-ttu-id="efb4c-789">Questa operazione viene in genere definita in termini di valore di CIE XYZ o CIELAB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-789">This is typically defined in terms of CIEXYZ or CIELAB value.</span></span>

<span data-ttu-id="efb4c-790">In genere, viene usata una destinazione IT 8,7/3 contenente le patch CMYK.</span><span class="sxs-lookup"><span data-stu-id="efb4c-790">Typically, an IT8.7/3 target containing CMYK patches is used.</span></span> <span data-ttu-id="efb4c-791">Le patch sono costituite dal campionamento dello spazio CMYK in modo ben definito in modo da formare una griglia rettangolare (con spaziatura non uniforme in C, M, Y e K).</span><span class="sxs-lookup"><span data-stu-id="efb4c-791">The patches consist of sampling of the CMYK space in a well-defined manner so that a rectangular grid (with non-uniform spacing in C, M, Y and K) is formed.</span></span> <span data-ttu-id="efb4c-792">Ogni patch viene quindi misurata con un colorimetro o uno spettrofotometro.</span><span class="sxs-lookup"><span data-stu-id="efb4c-792">Each patch is then measured with a colorimeter or spectrophotometer.</span></span> <span data-ttu-id="efb4c-793">Le misurazioni nei valori CIE XYZ formano quindi una tabella di ricerca (LUT), da cui viene compilato un modello empirico della stampante usando il metodo di interpolazione di Sakamoto.</span><span class="sxs-lookup"><span data-stu-id="efb4c-793">The measurements in CIEXYZ values then form a lookup table (LUT), from which an empirical model of the printer is built using Sakamoto's interpolation method.</span></span> <span data-ttu-id="efb4c-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="efb4c-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="efb4c-795">I due brevetti citati sono scaduti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-795">The two patents mentioned have expired.</span></span>

<span data-ttu-id="efb4c-796">I requisiti specifici per gli esempi di misurazione CMYK necessari per l'accettazione di un profilo del modello di dispositivo come validi dal modello di dispositivo Baseline Printer CMYK sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-796">Specific requirements for the CMYK measurement samples necessary for a device model profile to be accepted as valid by the CMYK printer baseline device model are as follows.</span></span> <span data-ttu-id="efb4c-797">Il set di esempi è descritto più chiaramente come un set di cubi di esempio CMY, ognuno associato a un livello K specifico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-797">(The sample set is most clearly described as a set of CMY sample cubes, each associated with a specific K level.)</span></span>

-   <span data-ttu-id="efb4c-798">È necessario fornire almeno cubi CMY validi per i livelli K = 0 e K = 100.</span><span class="sxs-lookup"><span data-stu-id="efb4c-798">At minimum, valid CMY cubes must be provided for the K = 0 and K = 100 levels.</span></span>
-   <span data-ttu-id="efb4c-799">È possibile che i livelli intermedi K non siano distanziati in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="efb4c-799">Intermediate K levels may be non-uniformly spaced.</span></span>
-   <span data-ttu-id="efb4c-800">Qualsiasi livello intermedio K senza un cubo CMY valido verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-800">Any intermediate K level without a valid CMY cube will be ignored.</span></span>
-   <span data-ttu-id="efb4c-801">I cubi CMY possono usare intervalli di campionamento non uniformi (spaziatura della griglia), ma lo stesso set di intervalli di campionamento deve essere usato in tutte le dimensioni C, M e Y del cubo CMY per un determinato livello K.</span><span class="sxs-lookup"><span data-stu-id="efb4c-801">The CMY cubes may use non-uniform sample intervals (grid spacing), but the same set of sample intervals must be used in all of the C,M, and Y dimensions in the CMY cube for a given K level.</span></span>
-   <span data-ttu-id="efb4c-802">Ogni cubo CMY di livello K può usare un numero e una spaziatura diversi di intervalli di campionamento.</span><span class="sxs-lookup"><span data-stu-id="efb4c-802">Each K level CMY cube can use a different number and spacing of sample intervals.</span></span>
-   <span data-ttu-id="efb4c-803">Tutti i cubi CMY devono contenere gli "angoli" del cubo CMY, ovvero i campioni CMY a \[ 0, 0, 0 \] , \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .</span><span class="sxs-lookup"><span data-stu-id="efb4c-803">All CMY cubes must contain the "corners" of the CMY cube, that is, CMY samples at \[0,0,0\], \[0,0,100\], \[0,100,0\], \[100,0,0\], \[0,100,100\], \[100,0,100\], \[100,100, 0\], \[100,100,100\].</span></span>
-   <span data-ttu-id="efb4c-804">Tutti i livelli di griglia CMY intermedi devono essere campionati in modo completo in ogni canale.</span><span class="sxs-lookup"><span data-stu-id="efb4c-804">Any intermediate CMY grid levels must be fully sampled in each channel.</span></span> <span data-ttu-id="efb4c-805">In altre parole, un campione deve esistere in ogni intersezione di griglia 3D all'interno del cubo CMY.</span><span class="sxs-lookup"><span data-stu-id="efb4c-805">In other words, a sample must exist at each 3-D grid intersection within the CMY cube.</span></span>
-   <span data-ttu-id="efb4c-806">Per i cubi K = 0 e K = 100 CMY, i Cubi 2x2x2 "solo gli angoli" sono i cubi minimo accettati come validi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-806">For the K = 0 and K = 100 CMY cubes, 2x2x2 "corners-only" cubes are the minimum accepted as valid.</span></span>

    <span data-ttu-id="efb4c-807">\[Nota: per K = 0 e K = 100 livelli, un cubo 3x3x3 CMY verrà elaborato come un cubo 2x2x2 "solo angoli"; il livello di campionamento intermedio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-807">\[NOTE: for K=0 and K=100 levels, a 3x3x3 CMY cube will be processed as a 2x2x2 "corners-only" cube; the intermediate sample level is ignored.</span></span> <span data-ttu-id="efb4c-808">in 4x4x4 e nei cubi più grandi saranno usati tutti gli esempi in griglia.\]</span><span class="sxs-lookup"><span data-stu-id="efb4c-808">4x4x4 and larger cubes will have all on-grid samples used.\]</span></span>

-   <span data-ttu-id="efb4c-809">Per i livelli intermedio K, i cubi 4x4x4 CMY sono i cubi minimo accettati come validi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-809">For intermediate K levels, 4x4x4 CMY cubes are the minimum accepted as valid.</span></span>

<span data-ttu-id="efb4c-810">Un profilo di qualità elevata utilizzerà griglie di campionamento più sottili del valore minimo necessario per la validità, in genere 9x9x9x9 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="efb4c-810">A high-quality profile will use finer sampling grids than the minimum required for validity, usually 9x9x9x9 or higher.</span></span> <span data-ttu-id="efb4c-811">Gli esempi di IT 8.7/3, IT 8,7/4 e ECI targets producono i profili dei modelli di dispositivo (DMPs) validi per il modello di dispositivo Baseline della stampante CMYK.</span><span class="sxs-lookup"><span data-stu-id="efb4c-811">The samples from the IT8.7/3, IT8.7/4, and ECI targets produce valid device model profiles (DMPs)for the CMYK printer baseline device model.</span></span> <span data-ttu-id="efb4c-812">Sebbene questo modello di dispositivo sia in grado di ignorare gli esempi estranei (fuori griglia) in queste destinazioni, non è garantito che sia possibile eseguire questa operazione per altre destinazioni, quindi è consigliabile rimuovere gli esempi estranei dai set di misure che passano ai profili per questo modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-812">While this device model is able to ignore the extraneous (off-grid) samples in these targets, it is not guaranteed to be able to do so for other targets, and so, it is recommended that extraneous samples be removed from measurement sets going into profiles for this device model.</span></span>

<span data-ttu-id="efb4c-813">L'inversione del modello di stampante presenta maggiori difficoltà.</span><span class="sxs-lookup"><span data-stu-id="efb4c-813">The inversion of the printer model presents more difficulties.</span></span> <span data-ttu-id="efb4c-814">Dato un colore di input in CIECAM, si verifica se questo colore si trova all'interno del gamut della stampante.</span><span class="sxs-lookup"><span data-stu-id="efb4c-814">Given an input color in CIECAM, there is a question of whether this color is within the printer gamut.</span></span> <span data-ttu-id="efb4c-815">Esiste anche il problema relativo alla disposizione dei punti nello spazio di aspetto dei colori.</span><span class="sxs-lookup"><span data-stu-id="efb4c-815">There is also the issue regarding the arrangement of points in the color appearance space.</span></span> <span data-ttu-id="efb4c-816">Sebbene sia possibile disporre i valori CMYK in modo che rientrino in una griglia rettangolare, come avviene nella destinazione 8,7/3, lo stesso non può essere detto dei colori stampati risultanti perché si trovano nello spazio di aspetto del colore.</span><span class="sxs-lookup"><span data-stu-id="efb4c-816">While we can arrange the CMYK values to fall on a rectangular grid, as is done in the IT8.7/3 target, the same cannot be said of the resulting printed colors as they are situated in the color appearance space.</span></span> <span data-ttu-id="efb4c-817">In generale, sono sparse nello spazio di aspetto dei colori senza motivo particolare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-817">In general, they are scattered in the color appearance space with no particular pattern.</span></span>

<span data-ttu-id="efb4c-818">Esistono in genere due approcci al problema di inversione dei punti sparsi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-818">There are generally two approaches to the inversion problem of scattered points.</span></span> <span data-ttu-id="efb4c-819">Un approccio consiste nell'usare una suddivisione geometrica della gamma di stampanti usando solidi tridimensionali primari, ad esempio tetraedri.</span><span class="sxs-lookup"><span data-stu-id="efb4c-819">One approach is to use a geometric subdivision of the printer gamut using elementary 3-dimensional solids, such as tetrahedra.</span></span> <span data-ttu-id="efb4c-820">Una suddivisione del gamut della stampante nello spazio di aspetto dei colori può essere indotta dalla suddivisione corrispondente dello spazio CMY (K), vedere Hung \[ 93 \] , Kang \[ 97 \] . Questo approccio offre il vantaggio della semplicità computazionale.</span><span class="sxs-lookup"><span data-stu-id="efb4c-820">A subdivision of the printer gamut in the color appearance space can be induced from the corresponding subdivision of the CMY(K) space, see Hung\[93\], Kang\[97\].This approach has the advantage of computational simplicity.</span></span> <span data-ttu-id="efb4c-821">Nel caso di un tetraedro, solo quattro punti vengono usati in un'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-821">In the case of a tetrahedron, only four points are used in an interpolation.</span></span> <span data-ttu-id="efb4c-822">D'altra parte, il risultato dipende molto da alcuni punti, il che significa che un errore di misurazione avrà un effetto significativo sul risultato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-822">On the other hand, the result depends heavily on a few points, which means that a measurement error will have a significant effect on the result.</span></span> <span data-ttu-id="efb4c-823">L'interpolatore tende anche a non essere uniforme.</span><span class="sxs-lookup"><span data-stu-id="efb4c-823">The interpolant also tends to be not as smooth.</span></span> <span data-ttu-id="efb4c-824">Il secondo approccio non presuppone alcuna suddivisione ed è basato sulla tecnica di interpolazione dei dati sparsi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-824">The second approach does not assume any subdivision, and is based on the technique of scattered data interpolation.</span></span> <span data-ttu-id="efb4c-825">Un esempio classico è la tecnica dell'interpolazione di Shepard o del metodo ponderato inverso (vedere Shepard \[ 68 \] ).</span><span class="sxs-lookup"><span data-stu-id="efb4c-825">A classical example is the technique of Shepard interpolation, or inverse weighted method (See Shepard \[68\]).</span></span> <span data-ttu-id="efb4c-826">In questo caso, diversi punti che racchiudono il punto di input vengono scelti in qualche modo, ognuno assegna un peso, generalmente proporzionale alla distanza e l'interpolazione viene considerata come la media ponderata dei punti adiacenti.</span><span class="sxs-lookup"><span data-stu-id="efb4c-826">Here, several points surrounding the input point are chosen in some manner, each assigned a weight, usually inversely proportional to the distance, and the interpolant is taken as the weighted average of the neighboring points.</span></span> <span data-ttu-id="efb4c-827">In questo approccio, la scelta dei punti adiacenti è fondamentale per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="efb4c-827">In this approach, the choice of neighboring points is paramount to performance.</span></span> <span data-ttu-id="efb4c-828">Sebbene un numero troppo basso di punti possa rendere l'interoperabilità non accurata e non smussata, troppi punti impongono un elevato costo computazionale, in quanto i pesi sono in genere funzioni non lineari e costose da calcolare.</span><span class="sxs-lookup"><span data-stu-id="efb4c-828">While too few points can render the interpolant inaccurate and non-smooth, too many points impose a high computational cost, as the weights are typically non-linear functions and costly to compute.</span></span>

<span data-ttu-id="efb4c-829">I due approcci descritti in precedenza presentano problemi.</span><span class="sxs-lookup"><span data-stu-id="efb4c-829">The two approaches described above both have problems.</span></span> <span data-ttu-id="efb4c-830">L'approccio di suddivisione dipende dal fatto che i dati siano ragionevolmente privi di rumore e, in genere, l'interpolazione non è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="efb4c-830">The subdivision approach depends critically on the data being reasonably void of noise, and generally the interpolant is not very smooth.</span></span> <span data-ttu-id="efb4c-831">L'interpolazione dei dati sparse è più tollerante al rumore dei dati e in genere fornisce un'interpolazione più uniforme, ma è più costosa dal punto di vista del calcolo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-831">The scattered data interpolation is more tolerant to data noise, and generally gives a smoother interpolant, but it is computationally more expensive.</span></span>

<span data-ttu-id="efb4c-832">La nuova CTE accetta un approccio alternativo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-832">The new CTE takes an alternative approach.</span></span> <span data-ttu-id="efb4c-833">Il dispositivo CMYK viene considerato come una raccolta di diversi dispositivi CMY, ognuno dei quali ha un valore specifico di nero (K).</span><span class="sxs-lookup"><span data-stu-id="efb4c-833">The CMYK device is treated as a collection of several CMY devices, each of which has a specific value of black (K).</span></span> <span data-ttu-id="efb4c-834">Usando un algoritmo di selezione che accetta come parametri luminosità e Chroma, viene scelto un livello di nero.</span><span class="sxs-lookup"><span data-stu-id="efb4c-834">Using a selection algorithm that takes as parameters lightness and chroma, a level of black is chosen.</span></span> <span data-ttu-id="efb4c-835">I valori CMY vengono ottenuti dall'inversione della tabella CMY corrispondente alla tabella Luv usando i metodi Newton usati altrove dall'algoritmo di stampa RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-835">The CMY values are obtained by inversion of the corresponding CMY to Luv table using the Newton methods employed elsewhere by the RGB printer algorithm.</span></span>

<span data-ttu-id="efb4c-836">Seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="efb4c-836">Use the following steps.</span></span>

1.  <span data-ttu-id="efb4c-837">Stampare la destinazione di caratterizzazione, ovvero la destinazione 8.7/3, oppure una destinazione contenente il campionamento dello spazio CMYK a intervalli regolari o irregolari.</span><span class="sxs-lookup"><span data-stu-id="efb4c-837">Print the characterization target, which is either the IT8.7/3 target, or a target containing sampling of the CMYK space at regularly or irregularly spaced intervals.</span></span>
2.  <span data-ttu-id="efb4c-838">Misurare la destinazione usando uno spettrofotometro e convertire le misurazioni nello spazio CIELUV.</span><span class="sxs-lookup"><span data-stu-id="efb4c-838">Measure the target using a spectrophotometer, and convert the measurements to CIELUV space.</span></span>
3.  <span data-ttu-id="efb4c-839">Costruire la mappa in diretta da CMYK a Luv.</span><span class="sxs-lookup"><span data-stu-id="efb4c-839">Construct the forward map from CMYK to Luv.</span></span>
4.  <span data-ttu-id="efb4c-840">Usare la mappa in linea per costruire un set di CMY a Luv Maps per un intervallo di valori K.</span><span class="sxs-lookup"><span data-stu-id="efb4c-840">Use the forward map to construct a set of CMY to Luv maps for a range of K values.</span></span>
5.  <span data-ttu-id="efb4c-841">Per qualsiasi valore di input Luv, il valore CMYK corrispondente viene ottenuto selezionando una delle mappe costruite nel passaggio 4 precedente e invertendo l'uso del metodo di Newton per ottenere un set di colori CMY associato al valore K selezionato.</span><span class="sxs-lookup"><span data-stu-id="efb4c-841">For any input Luv value, the corresponding CMYK value is obtained by selecting one of the maps constructed in step 4 above and inverting using Newton's method to obtain a CMY colorant set to accompany the K value selected.</span></span>

<span data-ttu-id="efb4c-842">I passaggi 1 e 2, ovvero le procedure standard, vengono eseguiti da un programma di profilatura che non fa parte della nuova CTE.</span><span class="sxs-lookup"><span data-stu-id="efb4c-842">Steps 1 and 2, which are standard procedures, are performed by a profiling program that is not part of the new CTE.</span></span> <span data-ttu-id="efb4c-843">La destinazione IT 8,7/3 contiene un campionamento ragionevolmente dettagliato di tutti i valori CMYK a diversi livelli di C, M, Y e K. in alternativa, è possibile usare una destinazione personalizzata con campionamento uniforme dei canali C, M, Y e K.</span><span class="sxs-lookup"><span data-stu-id="efb4c-843">The IT8.7/3 target contains a reasonably detailed sampling of all the CMYK values at various levels of C, M, Y, and K. Alternatively, a custom target with uniform sampling of the C, M, Y, and K channels can be used.</span></span> <span data-ttu-id="efb4c-844">Dopo la stampa della destinazione, è possibile usare uno spettrofotometro o un colorimetro per misurare il valore XYZ di ogni patch e il valore XYZ può essere convertito nel valore Luv usando il modello CIELUV.</span><span class="sxs-lookup"><span data-stu-id="efb4c-844">After the target is printed, a spectrophotometer or colorimeter can be used to measure the XYZ value of each patch, and the XYZ value can be converted to the Luv value using the CIELUV model.</span></span>

<span data-ttu-id="efb4c-845">Passaggio 3: la costruzione della mappa in avanti da CMYK a Luv può essere realizzata applicando qualsiasi tecnica di interpolazione nota, ad esempio tetraedrica o metodo multilineare, sulla griglia rettangolare nello spazio CMYK.</span><span class="sxs-lookup"><span data-stu-id="efb4c-845">Step 3, construction of the forward map from CMYK to Luv, can be achieved by applying any known interpolation technique, such as tetrahedral or multilinear method, on the rectangular grid in CMYK space.</span></span> <span data-ttu-id="efb4c-846">Nella nuova CTE viene utilizzata un'interpolazione tetraedrica a 4 dimensioni.</span><span class="sxs-lookup"><span data-stu-id="efb4c-846">In the new CTE, a 4-dimensional tetrahedral interpolation is used.</span></span> <span data-ttu-id="efb4c-847">Poiché le griglie di campionamento CMY sono generalmente diverse a seconda del livello K, tuttavia, viene usata una tecnica di supercampionamento, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="efb4c-847">Because the CMY sampling grids are generally different on each level of K, however, we use a technique of super-sampling, as detailed below.</span></span> <span data-ttu-id="efb4c-848">Per un determinato punto CMYK, i livelli sandwich K vengono innanzitutto determinati in base al valore K.</span><span class="sxs-lookup"><span data-stu-id="efb4c-848">For a given CMYK point, the sandwiching K levels are first determined based on the K value.</span></span> <span data-ttu-id="efb4c-849">Introdurre quindi una "Supergrid" a ogni livello K che rappresenta un'Unione delle griglie CMY in ognuno dei due livelli K.</span><span class="sxs-lookup"><span data-stu-id="efb4c-849">Then introduce a "super-grid" on each K level that is a union of the CMY grids on each of the two K levels.</span></span> <span data-ttu-id="efb4c-850">A ogni livello K, il valore Luv di qualsiasi punto di griglia appena introdotto viene ottenuto da un'interpolazione tetraedrica tridimensionale all'interno del livello K.</span><span class="sxs-lookup"><span data-stu-id="efb4c-850">On each K level, the Luv value of any newly introduced grid point is obtained by a 3-dimensional tetrahedral interpolation within that K level.</span></span> <span data-ttu-id="efb4c-851">Infine, in questa nuova griglia viene eseguita un'interpolazione tetraedrica a 4 dimensioni per il punto CMYK specifico.</span><span class="sxs-lookup"><span data-stu-id="efb4c-851">Finally, a 4-dimensional tetrahedral interpolation for the specific CMYK point is performed on this new grid.</span></span>

![Diagramma che mostra il sovracampionamento.](images/cdmp-image163.png)

<span data-ttu-id="efb4c-853">**Figura 8** : supercampionamento</span><span class="sxs-lookup"><span data-stu-id="efb4c-853">**Figure 8** : Supersampling</span></span>

<span data-ttu-id="efb4c-854">Il passaggio 4 costruisce un set di tabelle di ricerca da CMY a Luv (LUTs).</span><span class="sxs-lookup"><span data-stu-id="efb4c-854">Step 4 constructs a set of CMY-to-Luv lookup tables (LUTs).</span></span> <span data-ttu-id="efb4c-855">La mappa in avanti costruita nel passaggio 3 viene chiamata ripetutamente per ricampionare lo spazio CMYK.</span><span class="sxs-lookup"><span data-stu-id="efb4c-855">The forward map constructed in Step 3 is called repeatedly to resample the CMYK space.</span></span> <span data-ttu-id="efb4c-856">Lo spazio dei colori CMYK viene campionato usando una spaziatura uniforme di K e un campionamento di CMY diverso, ma ancora in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="efb4c-856">The CMYK color space is sampled using an even spacing of K and a different, but still evenly spaced, sampling of CMY.</span></span>

<span data-ttu-id="efb4c-857">Il passaggio 5 è una procedura per ottenere il valore CMYK usando LUTs costruito nel passaggio 4 per qualsiasi punto di Luv di input.</span><span class="sxs-lookup"><span data-stu-id="efb4c-857">Step 5 is a procedure to obtain the CMYK value using the LUTs constructed in Step 4 for any input Luv point.</span></span> <span data-ttu-id="efb4c-858">Viene scelto il valore appropriato di K analizzando la luminosità, nonché il grado di colore nell'Luv richiesto.</span><span class="sxs-lookup"><span data-stu-id="efb4c-858">The appropriate value of K is chosen by analyzing the lightness as well as the degree of color in the Luv requested.</span></span> <span data-ttu-id="efb4c-859">Dopo aver selezionato la tabella, i valori CMY vengono ottenuti dalla tabella usando il metodo di Newton, come illustrato in precedenza nel modello di dispositivo della stampante RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-859">After the table is selected, the CMY values are obtained from the table by using Newton's method (as documented under the RGB printer device model earlier).</span></span>

<span data-ttu-id="efb4c-860">Lo spazio CIELUV viene usato nel modello di stampante invece che in CIEJab, perché il modello di dispositivo deve essere basato esclusivamente sui dati colorimetrico disponibili nel DMP.</span><span class="sxs-lookup"><span data-stu-id="efb4c-860">CIELUV space is used in the printer model instead of CIEJab because the device model should be based solely on colorimetric data available in the DMP.</span></span> <span data-ttu-id="efb4c-861">Il DMP contiene dati colorimetrico per ogni patch misurata, incluso il punto per i supporti, quindi è possibile convertire i dati CIE XYZ in dati CIELUV.</span><span class="sxs-lookup"><span data-stu-id="efb4c-861">The DMP contains colorimetric data for each measured patch, including the media white point, so it is possible to convert CIEXYZ data into CIELUV data.</span></span> <span data-ttu-id="efb4c-862">Tuttavia, non è possibile eseguire la conversione in CIECAM02 JCh o jab, perché non è possibile accedere alle informazioni sulla condizione di visualizzazione nel DMP.</span><span class="sxs-lookup"><span data-stu-id="efb4c-862">However, it is not possible to convert to CIECAM02 JCh or Jab, because there is no access to the viewing condition information in the DMP.</span></span>

### <a name="rgb-projector-device-model-baseline"></a><span data-ttu-id="efb4c-863">Baseline modello di dispositivo proiettore RGB</span><span class="sxs-lookup"><span data-stu-id="efb4c-863">RGB Projector Device Model Baseline</span></span>

<span data-ttu-id="efb4c-864">Nota: molti proiettori RGB hanno più di una modalità operativa.</span><span class="sxs-lookup"><span data-stu-id="efb4c-864">Note: Many RGB projectors have more than one operating mode.</span></span> <span data-ttu-id="efb4c-865">In una modalità, che è spesso l'impostazione predefinita e potrebbe essere chiamata come "presentazione", la risposta al colore del proiettore è ottimizzata per la massima luminosità.</span><span class="sxs-lookup"><span data-stu-id="efb4c-865">In one mode, which is often the default and might be called something like "presentation," the color response of the projector is optimized for maximum brightness.</span></span> <span data-ttu-id="efb4c-866">Tuttavia, in questa modalità, il proiettore perde la possibilità di riprodurre colori chiari, leggermente cromatici, ad esempio i gialli pallidi e alcuni toni di carne.</span><span class="sxs-lookup"><span data-stu-id="efb4c-866">However, in this mode, the projector loses the ability to reproduce light, slightly chromatic colors such as pale yellows and some flesh tones.</span></span> <span data-ttu-id="efb4c-867">In un'altra modalità, spesso denominata "film", "video" o "sRGB", il proiettore è ottimizzato per la riproduzione di immagini realistiche e scene naturali.</span><span class="sxs-lookup"><span data-stu-id="efb4c-867">In another mode, often called "film," "video," or "sRGB," the projector is optimized for reproduction of realistic images and natural scenes.</span></span> <span data-ttu-id="efb4c-868">In questa modalità, la luminosità massima viene comunicata per migliorare la qualità complessiva della riproduzione dei colori.</span><span class="sxs-lookup"><span data-stu-id="efb4c-868">In this mode, maximum brightness is traded off to improve the overall quality of the color reproduction.</span></span> <span data-ttu-id="efb4c-869">Per ottenere una riproduzione dei colori soddisfacente con i proiettori RGB, è necessario posizionare il proiettore in una modalità in cui è possibile riprodurre una gamma uniforme di colori.</span><span class="sxs-lookup"><span data-stu-id="efb4c-869">To obtain satisfactory color reproduction with RGB projectors, it is necessary to place the projector in a mode where a smooth gamut of colors can be reproduced.</span></span>

![Diagramma che mostra un modello di dispositivo D L P.](images/cdmp-image167.png)

<span data-ttu-id="efb4c-871">**Figura 9** : modello di dispositivo DLP</span><span class="sxs-lookup"><span data-stu-id="efb4c-871">**Figure 9** : DLP device model</span></span>

<span data-ttu-id="efb4c-872">Un valore RGB in ingresso passa attraverso due percorsi computazionali.</span><span class="sxs-lookup"><span data-stu-id="efb4c-872">An incoming RGB value passes through two computational pathways.</span></span> <span data-ttu-id="efb4c-873">Il primo è il modello Matrix, che restituisce un valore XYZ.</span><span class="sxs-lookup"><span data-stu-id="efb4c-873">The first is the matrix model, which results in an XYZ value.</span></span> <span data-ttu-id="efb4c-874">Questa operazione è seguita immediatamente dalla conversione da XYZ a Luv.</span><span class="sxs-lookup"><span data-stu-id="efb4c-874">This is immediately followed by the conversion from XYZ to Luv.</span></span> <span data-ttu-id="efb4c-875">Il secondo è l'interpolazione LUT non uniforme mediante l'interpolazione di tetraedrica.</span><span class="sxs-lookup"><span data-stu-id="efb4c-875">The second is the non-uniform LUT interpolation using tetrahedral interpolation.</span></span> <span data-ttu-id="efb4c-876">L'output dell'interpolazione si trova già nello spazio Luv per costruzione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-876">The output of the interpolation is already in Luv space by construction.</span></span> <span data-ttu-id="efb4c-877">Per ottenere il valore Luv stimato vengono aggiunti i due output.</span><span class="sxs-lookup"><span data-stu-id="efb4c-877">The two outputs are added to obtain the predicted Luv value.</span></span> <span data-ttu-id="efb4c-878">Viene infine convertito in XYZ, ovvero l'output previsto del modello colorimetrico per il dispositivo DLP.</span><span class="sxs-lookup"><span data-stu-id="efb4c-878">This is finally converted to XYZ, which is the expected output of the colorimetric model for the DLP device.</span></span>

<span data-ttu-id="efb4c-879">Poiché i proiettori sono dispositivi di visualizzazione, supportano anche l'inversione del modello, ovvero la trasformazione da XYZ a RGB.</span><span class="sxs-lookup"><span data-stu-id="efb4c-879">Since projectors are display devices, they also support the inversion of the model, that is, the transform from XYZ to RGB.</span></span> <span data-ttu-id="efb4c-880">Poiché il modello di dispositivo trasforma lo spazio RGB nello spazio XYZ, che sono entrambi tridimensionali, l'inversione è equivalente alla risoluzione di tre equazioni non lineari in tre incognite.</span><span class="sxs-lookup"><span data-stu-id="efb4c-880">Because the device model transforms RGB space to XYZ space, which are both three dimensional, inversion is equivalent to solving three nonlinear equations in three unknowns.</span></span> <span data-ttu-id="efb4c-881">Questa operazione può essere eseguita dalle tecniche standard di risoluzione delle equazioni, ad esempio Newton-Raphson.</span><span class="sxs-lookup"><span data-stu-id="efb4c-881">This can done by standard equation solving techniques, such as Newton-Raphson.</span></span> <span data-ttu-id="efb4c-882">È preferibile, tuttavia, convertire prima XYZ in Luv, quindi invertire il Luv nella trasformazione RGB, perché lo spazio Luv è più percettivamente lineare dello spazio XYZ.</span><span class="sxs-lookup"><span data-stu-id="efb4c-882">It is preferable, however, to first convert XYZ to Luv, and then invert the Luv To RGB transform, because Luv space is more perceptually linear than XYZ space.</span></span>

### <a name="icc-device-model-baseline"></a><span data-ttu-id="efb4c-883">Baseline del modello di dispositivo ICC</span><span class="sxs-lookup"><span data-stu-id="efb4c-883">ICC Device Model Baseline</span></span>

<span data-ttu-id="efb4c-884">L'interoperabilità del flusso di lavoro ICC viene abilitata mediante la creazione di un profilo del modello di dispositivo di baseline del dispositivo ICC speciale che archivia l'oggetto profilo e crea una trasformazione ICC usando un profilo no-op XYZ.</span><span class="sxs-lookup"><span data-stu-id="efb4c-884">The CITE ICC workflow interoperability is enabled by creating a special ICC device baseline device model profile that stores the profile object and creates a ICC transform using a no-op XYZ profile.</span></span> <span data-ttu-id="efb4c-885">Questa trasformazione viene quindi utilizzata per la conversione tra i colori del dispositivo e del CIE XYZ.</span><span class="sxs-lookup"><span data-stu-id="efb4c-885">This transform is then used to translate between device and CIEXYZ colors.</span></span>

![Diagramma che illustra l'interoperabilità del flusso di lavoro c I T E I c c.](images/cdmp-image168.png)

<span data-ttu-id="efb4c-887">**Figura 10** : citare l'interoperabilità del flusso di lavoro ICC</span><span class="sxs-lookup"><span data-stu-id="efb4c-887">**Figure 10** : CITE ICC Workflow Interoperability</span></span>

## <a name="related-topics"></a><span data-ttu-id="efb4c-888">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efb4c-888">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efb4c-889">Concetti di base sulla gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="efb4c-889">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="efb4c-890">Schemi e algoritmi del sistema di colori Windows</span><span class="sxs-lookup"><span data-stu-id="efb4c-890">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





