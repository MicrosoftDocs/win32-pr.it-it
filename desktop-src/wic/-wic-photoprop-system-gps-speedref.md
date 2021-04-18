---
description: Criteri per i metadati delle foto per la proprietà System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Criteri per i metadati delle foto di System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315972"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. SpeedRef

Criteri per i metadati delle foto per la proprietà [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ SpeedRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ LPWSTR è preferibile, ma \_ anche VT LPSTR è accettato.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      | Formato del disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      |         |
|-------|---------------------------|---------|
| 1     | /IFD/GPS/{ushort = 12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{ushort = 12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
