---
title: Struttura DDS_PIXELFORMAT (DDS. h)
description: Formato pixel superficie.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- Struttura DDS_PIXELFORMAT DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322291"
---
# <a name="dds_pixelformat-structure"></a>\_Struttura PIXELFORMAT PIXELFORMAT

Formato pixel superficie.

## <a name="syntax"></a>Sintassi


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Dimensioni della struttura; impostare su 32 (byte).

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valori che indicano il tipo di dati presenti sulla superficie.



| Flag              | Descrizione                                                                                                                                                                                                                                | Valore   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| \_ALPHAPIXELS DDPF | La trama contiene dati alfa; **dwRGBAlphaBitMask** contiene dati validi.                                                                                                                                                                    | 0x1     |
| DDPF \_ alfa       | Usato in alcuni file DDS meno recenti per il canale alfa solo dati non compressi (dwRGBBitCount contiene il canale alfa bitCount; dwABitMask contiene dati validi)                                                                                  | 0x2     |
| \_fourcc DDPF      | La trama contiene dati RGB compressi; **dwFourCC** contiene dati validi.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | La trama contiene dati RGB non compressi; **dwRGBBitCount** e le maschere RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contengono dati validi.                                                                                           | 0x40    |
| \_YUV DDPF         | Usato in alcuni file DDS precedenti per i dati non compressi YUV (dwRGBBitCount contiene il numero di bit YUV; dwRBitMask contiene la maschera Y, dwGBitMask contiene l'U mask, dwBBitMask contiene V mask)                                          | 0x200   |
| \_luminanza DDPF   | Usato in alcuni file DDS meno recenti per i dati non compressi del colore a canale singolo (dwRGBBitCount contiene il numero di bit del canale di luminanza; dwRBitMask contiene la maschera del canale). Può essere combinato con DDPF \_ ALPHAPIXELS per un file DDS con due canali. | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Codici di quattro caratteri per la specifica di formati compressi o personalizzati. I valori possibili includono: *DXT1*, *DXT2*, *DXT3*, *DXT4* o *DXT5*. Un FourCC di DX10 indica prescense dell'intestazione [**DDS \_ \_ DXT10**](dds-header-dxt10.md) intestazione estesa e il membro dxgiFormat di tale struttura indica il formato true. Quando si utilizza un codice di quattro caratteri, dwFlags deve includere *DDPF \_ fourcc*.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di bit in un formato RGB (possibilmente incluso Alpha). Valido quando **dwFlags** include *DDPF \_ RGB*, *DDPF \_ Luminance* o *DDPF \_ YUV*.

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera rossa (o lumiannce o Y) per la lettura dei dati di colore. Ad esempio, dato il formato A8R8G8B8, la maschera rossa è 0x00FF0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera verde (o U) per la lettura dei dati di colore. Ad esempio, dato il formato A8R8G8B8, la maschera verde è 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera blu (o V) per la lettura dei dati di colore. Ad esempio, dato il formato A8R8G8B8, la maschera blu è 0x000000FF.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera Alpha per la lettura di dati alfa. dwFlags deve includere *DDPF \_ ALPHAPIXELS* o *DDPF \_ Alpha*. Ad esempio, in base al formato A8R8G8B8, alpha mask è 0xFF000000.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per archiviare i formati DXGI, ad esempio i dati a virgola mobile, usare un **dwFlags** di DDPF \_ fourcc e impostare **dwFourCC** su',' X ',' 1',' 0'. Usare l'intestazione [**DDS \_ header \_ DXT10**](dds-header-dxt10.md) Extension per archiviare il formato DXGI nel membro **dxgiFormat** .

Si noti che esistono varianti non standard dei file DDS in cui **dwFlags** ha DDPF \_ fourcc e il valore **dwFourCC** è impostato direttamente su un valore di enumerazione di formato D3DFORMAT o DXGI \_ . Non è possibile evitare ambiguità tra i valori di formato D3DFORMAT e DXGI \_ usando questo schema non standard, quindi è invece consigliabile usare l'intestazione di estensione DX10.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento per DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

