---
description: Criteri per i metadati delle foto per la proprietà System. copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Criteri per i metadati della foto System. Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317888"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Criteri per i metadati della foto System. Copyright

Criteri per i metadati delle foto per la proprietà [System. Copyright](../properties/props-system-copyright.md) .

### <a name="pkey"></a>PKEY

\_Copyright pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

string

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                      | Formato disco |
|-------|-------------------------------------------|-------------|
|       | /App1/IFD/{ushort = 33432}                  | ascii       |
|       | avviso/App13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /XMP/ <xmpalt> DC: diritti              | unicode     |
|       | /XMP/DC: diritti                            | unicode     |
|       | avviso/App13/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                      | Formato disco |
|-------|-------------------------------------------|-------------|
|       | /XMP/DC: diritti                            | unicode     |
|       | /XMP/ <xmpalt> DC: diritti              | unicode     |
|       | avviso/App13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /App1/IFD/{ushort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                      |
|-------|-------------------------------------------|
|       | /XMP/DC: diritti                            |
|       | avviso/App13/IRB/8bimiptc/IPTC/Copyright |
|       | /App1/IFD/{ushort = 33432}                  |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
|       | /IFD/{ushort = 33432}                     | ascii       |
|       | avviso/IFD/IPTC/Copyright              |             |
|       | /IFD/XMP/ <xmpalt> DC: diritti        | unicode     |
|       | /IFD/XMP/DC: diritti                      | unicode     |
|       | avviso/IFD/IPTC/Copyright              |             |
|       | avviso/IFD/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                    | Formato disco |
|-------|-----------------------------------------|-------------|
|       | /IFD/XMP/DC: diritti                      | unicode     |
|       | /IFD/XMP/ <xmpalt> DC: diritti        | unicode     |
|       | avviso/IFD/IPTC/Copyright              |             |
|       | avviso/IFD/IRB/8bimiptc/IPTC/Copyright |             |
|       | /IFD/{ushort = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                    |
|-------|-----------------------------------------|
|       | /IFD/XMP/DC: diritti                      |
|       | avviso/IFD/IPTC/Copyright              |
|       | avviso/IFD/IRB/8bimiptc/IPTC/Copyright |
|       | /IFD/{ushort = 33432}                     |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
