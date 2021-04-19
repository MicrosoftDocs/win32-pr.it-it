---
title: Schema di calibrazione WCS
description: Questo argomento descrive lo schema di calibrazione WCS che espande il profilo del modello del dispositivo a colori WCS.
ms.assetid: 99f3e9e3-15b7-4bca-87cc-a3bf3b6d0112
keywords:
- Sistema di colori Windows (WCS), calibrazione
- WCS (sistema di colori Windows), calibrazione
- Gestione colori immagine, calibrazione
- gestione dei colori, calibrazione
- colori, calibrazione
- schemi, calibrazione
- Calibrazione WCS
- calibrazione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e859ab9d2b47355db063961004f17a8cc1537694
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320153"
---
# <a name="wcs-calibration-schema"></a>Schema di calibrazione WCS

Questo argomento descrive lo schema di calibrazione WCS che espande il [profilo del modello del dispositivo a colori WCS](wcs-color-device-model-profile-schema-and-algorithms.md).

## <a name="the-wcs-calibration-schema"></a>Schema di calibrazione WCS

La definizione dello schema seguente viene utilizzata per specificare le nuove definizioni di Windows 7 che supportano la calibrazione del [profilo del modello del dispositivo a colori WCS](wcs-color-device-model-profile-schema-and-algorithms.md) .


```C++
<?xml version="1.0" encoding="UTF-8"?>
<!--
  Copyright (C) Microsoft. All rights reserved. The Windows Color System
  color profile schemas may be used according to the terms of the license agreement
  available at https://www.microsoft.com/whdc/device/display/color/wcs_license.mspx.
  -->
<xs:schema
  xmlns:cal="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model Calibration profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="AdapterGammaConfiguration">
    <xs:choice>
      <xs:element name="ParameterizedCurves" type="wcs:ParameterizedCurvesType"/>
      <xs:element name="HDRToneResponseCurves" type="wcs:HDRToneResponseCurvesType"/>
    </xs:choice>
  </xs:complexType>

  <xs:complexType name="Calibration">
    <xs:sequence>
      <xs:element name="AdapterGammaConfiguration" type="cal:AdapterGammaConfiguration" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>

</xs:schema>
```



Per la compatibilità con Windows Vista, i profili contenenti tag di calibratura devono includere l'attributo `mc:Ignoreable="cdm_calibration"` .

 

 




