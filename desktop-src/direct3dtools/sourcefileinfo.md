---
description: Rappresenta informazioni su un file di codice sorgente.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura SourceFileInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39fdb9e7236dea1c04eb55614d9ea9833f398a94
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623127"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>Struttura SourceFileInfo

Rappresenta informazioni su un file di codice sorgente.

## <a name="syntax"></a>Sintassi


```C++
} SourceFileInfo;
```

## <a name="members"></a>Members

**Filename**  
Stringa COM che contiene il percorso del file di origine associato.

**checksumByteCount**  
Numero di byte nel checksum. Quando checkSumAlgorithm è uguale a CHECKSUMALGORITHM::md5, checkSumByteCount è 16. Quando checkSumAlgorithm è uguale a CHECKSUMALGORITHM::sha1, checkSumByteCount è 20.

**checkSumAlgorithm**  
Specifica l'algoritmo utilizzato per generare il checksum del file. Gli algoritmi supportati sono MD5 e SHA1. Per altre informazioni, vedere l'enumerazione CHECKSUMALGORITHM.

**checkSumFirstPart**  
Prima parte di 8 byte del checksum.

**checkSumSecondPart**  
Seconda parte a 8 byte del checksum.

**checkSumThirdPart**  
Terza parte a 8 byte del checksum.

**checkSumFourthPart**  
Quarta parte a 8 byte del checksum.

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



