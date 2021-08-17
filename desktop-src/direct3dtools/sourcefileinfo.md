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
ms.openlocfilehash: 9b6afd5f3b383aff5c6d5168b259b13fe4429ac40d5b19a21c8e2f6a207cecd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119235"
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
Prima parte del checksum a 8 byte.

**checkSumSecondPart**  
Seconda parte a 8 byte del checksum.

**checkSumThirdPart**  
Terza parte del checksum a 8 byte.

**checkSumFourthPart**  
Quarta parte del checksum a 8 byte.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



