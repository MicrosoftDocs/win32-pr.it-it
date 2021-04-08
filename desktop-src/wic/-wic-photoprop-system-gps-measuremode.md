---
description: Criteri per i metadati delle foto per la proprietà System. GPS. MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Criteri per i metadati delle foto di System. GPS. MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967635"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. MeasureMode

Criteri per i metadati delle foto per la proprietà [System. GPS. MeasureMode](../properties/props-system-gps-measuremode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ MeasureMode

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 10} |
| 2     | /xmp/exif:gpsmeasuremode  |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{ushort = 10}         |
| 2     | /ifd/xmp/exif:gpsmeasuremode |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. MeasureMode](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
