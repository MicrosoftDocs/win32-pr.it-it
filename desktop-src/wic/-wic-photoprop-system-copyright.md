---
description: Criteri dei metadati delle foto per la proprietà System.Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Criteri relativi ai metadati delle foto di System.Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00b57bc3523feaa29da9008340bd34c32401879a8fc4e872082bbdcddd1fdf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710814"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Criteri relativi ai metadati delle foto di System.Copyright

Criteri dei metadati delle foto per [la proprietà System.Copyright.](../properties/props-system-copyright.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Copyright

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

string

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                      | Formato disco |
|-------|-------------------------------------------|-------------|
|       | /app1/ifd/{ushort=33432}                  | ascii       |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /xmp/ <xmpalt> dc:rights              | unicode     |
|       | /xmp/dc:rights                            | unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                      | Formato disco |
|-------|-------------------------------------------|-------------|
|       | /xmp/dc:rights                            | unicode     |
|       | /xmp/ <xmpalt> dc:rights              | unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /app1/ifd/{ushort=33432}                  | ascii       |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                      |
|-------|-------------------------------------------|
|       | /xmp/dc:rights                            |
|       | /app13/irb/8bimiptc/iptc/copyright notice |
|       | /app1/ifd/{ushort=33432}                  |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
|       | /ifd/{ushort=33432}                     | ascii       |
|       | /ifd/iptc/copyright notice              |             |
|       | /ifd/xmp/ <xmpalt> dc:rights        | unicode     |
|       | /ifd/xmp/dc:rights                      | unicode     |
|       | /ifd/iptc/copyright notice              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
|       | /ifd/xmp/dc:rights                      | unicode     |
|       | /ifd/xmp/ <xmpalt> dc:rights        | unicode     |
|       | /ifd/iptc/copyright notice              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |
|       | /ifd/{ushort=33432}                     | ascii       |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                    |
|-------|-----------------------------------------|
|       | /ifd/xmp/dc:rights                      |
|       | /ifd/iptc/copyright notice              |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |
|       | /ifd/{ushort=33432}                     |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
