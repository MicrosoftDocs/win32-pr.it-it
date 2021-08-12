---
description: CABINETDLLVERSIONINFO contiene le informazioni sulla versione per Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Struttura CABINETDLLVERSIONINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9276a03d28bdfeee2b97b44e180bf190cbf20fc40ec58d0aafb44962a6e8fa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667984"
---
# <a name="cabinetdllversioninfo-structure"></a>Struttura CABINETDLLVERSIONINFO

\[Questa struttura contiene informazioni necessarie solo quando si usa la **funzione DllGetVersion,** che non è supportata. Questa documentazione viene fornita solo a scopo informativo.\]

**CABINETDLLVERSIONINFO contiene** le informazioni sulla versione per Cabinet.dll.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**cbStruct**
</dt> <dd>

Dimensioni della struttura, in byte.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Riservato.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Riservato.

</dd> <dt>

**dwFileVersionMS**
</dt> <dd>

Contiene i bit più significativi delle informazioni sulla versione. I bit 0-15 contengono la versione secondaria e i bit 16-31 contengono la versione principale.

</dd> <dt>

**dwFileVersionLS**
</dt> <dd>

Contiene i bit meno significativi delle informazioni sulla versione. I bit 0-15 contengono il numero di revisione e i bit 16-31 contengono il numero di build.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 



