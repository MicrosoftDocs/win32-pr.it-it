---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Criteri per i metadati delle foto di System. GPS. DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317879"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. DestLatitude

Criteri per i metadati delle foto per la proprietà [System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLatitude

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ vettore \| VT \_ R8

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ vettore \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. GPS. DestLatitudeNumerator e System. GPS. DestLatitudeDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 20} |
| 2     | /xmp/exif:gpsdestlatitude |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 20}          |
| 2     | /ifd/xmp/exif:gpsdestlatitude |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
