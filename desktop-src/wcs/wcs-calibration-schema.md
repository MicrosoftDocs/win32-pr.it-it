---
title: Schema di calibrazione WCS
description: In questo argomento viene descritto lo schema di calibrazione WCS che espande il profilo del modello di dispositivo a colori WCS.
ms.assetid: 99f3e9e3-15b7-4bca-87cc-a3bf3b6d0112
keywords:
- Windows Sistema di colori (WCS), calibrazione
- WCS (Windows Color System),calibrazione
- gestione dei colori delle immagini, calibrazione
- gestione dei colori, calibrazione
- colori, calibrazione
- schemi, calibrazione
- Calibrazione WCS
- Calibrazione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3744f8aa0190f09acf80b469ae01fddb035c48deda73d53871094ef9ece8e88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451421"
---
# <a name="wcs-calibration-schema"></a>Schema di calibrazione WCS

In questo argomento viene descritto lo schema di calibrazione WCS che espande il profilo del modello di dispositivo a colori [WCS](wcs-color-device-model-profile-schema-and-algorithms.md).

## <a name="the-wcs-calibration-schema"></a>Schema di calibrazione WCS

La definizione dello schema seguente viene utilizzata per specificare le nuove definizioni Windows 7 che supportano la calibrazione del profilo del modello di dispositivo a colori [WCS.](wcs-color-device-model-profile-schema-and-algorithms.md)


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



Per compatibilità con Windows Vista, i profili contenenti tag di calibrazione devono includere l'attributo `mc:Ignoreable="cdm_calibration"` .

 

 




