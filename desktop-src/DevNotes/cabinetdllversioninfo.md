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
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877653"
---
# <a name="cabinetdllversioninfo-structure"></a>Struttura CABINETDLLVERSIONINFO

\[Questa struttura contiene le informazioni necessarie solo quando si usa la funzione **DllGetVersion** , che non è supportata. Questa documentazione viene fornita solo a scopo informativo.\]

**CABINETDLLVERSIONINFO** contiene le informazioni sulla versione per Cabinet.dll.

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

Dimensioni, in byte, della struttura.

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

Contiene i bit più significativi delle informazioni sulla versione. BITS 0-15 contengono la versione secondaria e BITS 16-31 contengono la versione principale.

</dd> <dt>

**dwFileVersionLS**
</dt> <dd>

Contiene i bit meno significativi delle informazioni sulla versione. BITS 0-15 contengono il numero di revisione e BITS 16-31 contengono il numero di Build.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 



