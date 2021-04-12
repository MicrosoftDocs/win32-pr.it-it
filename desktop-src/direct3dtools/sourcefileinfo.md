---
description: Rappresenta le informazioni su un file di codice sorgente.
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
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481989"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>Struttura SourceFileInfo

Rappresenta le informazioni su un file di codice sorgente.

## <a name="syntax"></a>Sintassi


```C++
} SourceFileInfo;
```

## <a name="members"></a>Members

**fileName**  
Stringa COM che costituisce il FilePath del file di origine associato.

**checksumByteCount**  
Numero di byte nel checksum. Quando checkSumAlgorithm è uguale a CHECKSUMALGORITHM:: MD5, checkSumByteCount è 16. Quando checkSumAlgorithm è uguale a CHECKSUMALGORITHM:: SHA1, checkSumByteCount è 20.

**checkSumAlgorithm**  
Specifica l'algoritmo utilizzato per generare il checksum del file. Gli algoritmi supportati sono MD5 e SHA1. Per ulteriori informazioni, vedere l'enumerazione CHECKSUMALGORITHM.

**checkSumFirstPart**  
Prima parte a 8 byte del checksum.

**checkSumSecondPart**  
Parte secondo 8 byte del checksum.

**checkSumThirdPart**  
Terza parte del checksum a 8 byte.

**checkSumFourthPart**  
Quarta parte di 8 byte del checksum.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



