---
description: Criteri per i metadati delle foto per la proprietà System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Criteri dei metadati della foto System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312966"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>Criteri dei metadati della foto System. GPS. status

Criteri per i metadati delle foto per la proprietà [System. GPS. status](../properties/props-system-gps-status.md) .

### <a name="pkey"></a>PKEY

\_Stato pkey GPS \_

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



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 9} |
| 2     | /xmp/exif:gpsstatus      |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                    | Formato disco |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                    | Formato disco |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                    |
|-------|-------------------------|
| 1     | /IFD/GPS/{ushort = 9}     |
| 2     | /ifd/xmp/exif:gpsstatus |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
