---
description: Criteri per i metadati delle foto per la proprietà System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Criteri per i metadati di Photo System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315973"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>Criteri per i metadati di Photo System. GPS. Speed

Criteri per i metadati delle foto per la proprietà [System. GPS. Speed](../properties/props-system-gps-speed.md) .

### <a name="pkey"></a>PKEY

\_Velocità GPS \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. GPS. SpeedNumerator e System. GPS. SpeedDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 13} |
| 2     | /xmp/exif:gpsspeed        |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /IFD/GPS/{ushort = 13}   |
| 2     | /ifd/xmp/exif:gpsspeed |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. Speed](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
