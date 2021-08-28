---
title: DDS_PIXELFORMAT struttura (Dds.h)
description: Formato pixel della superficie.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT struttura DDS
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
ms.openlocfilehash: 08e2c8d4b5e30a3a5a9a039e27f5704019a6300c
ms.sourcegitcommit: 205567a2a76ad672a493a0203ff9d61271d9df98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/18/2021
ms.locfileid: "122358907"
---
# <a name="dds_pixelformat-structure"></a>Struttura \_ PIXELFORMAT DDS

Formato pixel della superficie.

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

Dimensioni della struttura; impostato su 32 (byte).

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valori che indicano il tipo di dati presenti nella superficie.



| Flag              | Descrizione                                                                                                                                                                                                                                | Valore   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| DDPF \_ ALPHAPIXELS | La trama contiene dati alfa. **dwRGBAlphaBitMask contiene** dati validi.                                                                                                                                                                    | 0x1     |
| DDPF \_ ALPHA       | Usato in alcuni file DDS meno recenti solo per i dati non compressi del canale alfa (dwRGBBitCount contiene il numero di bit del canale alfa; dwABitMask contiene dati validi)                                                                                  | 0x2     |
| DDPF \_ FOURCC      | La trama contiene dati RGB compressi. **dwFourCC contiene** dati validi.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | La trama contiene dati RGB non compressi. **dwRGBBitCount** e le maschere RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contengono dati validi.                                                                                           | 0x40    |
| DDPF \_ YUV         | Usato in alcuni file DDS meno recenti per i dati yuv non compressi (dwRGBBitCount contiene il numero di bit YUV; dwRBitMask contiene la maschera Y, dwGBitMask contiene la maschera U, dwBBitMask contiene la maschera V)                                          | 0x200   |
| DDPF \_ LUMINANCE   | Usato in alcuni file DDS meno recenti per i dati non compressi a colori a canale singolo (dwRGBBitCount contiene il numero di bit del canale di luminance; dwRBitMask contiene la maschera di canale). Può essere combinato con DDPF \_ ALPHAPIXELS per un file DDS a due canali. | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Codici a quattro caratteri per specificare formati compressi o personalizzati. I valori possibili includono: *DXT1,* *DXT2,* *DXT3,* *DXT4* o *DXT5.* Un elemento FourCC di DX10 indica la prescensione dell'intestazione estesa [**\_ DDS HEADER \_ DXT10**](dds-header-dxt10.md) e il membro dxgiFormat di tale struttura indica il formato vero. Quando si usa un codice di quattro caratteri, dwFlags deve includere *DDPF \_ FOURCC*.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di bit in un formato RGB (possibilmente incluso alpha). Valido quando **dwFlags** include *DDPF \_ RGB,* *DDPF \_ LUMINANCE* o *DDPF \_ YUV.*

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera rossa (o luminance o Y) per la lettura dei dati di colore. Ad esempio, dato il formato A8R8G8B8, la maschera rossa sarà 0x00ff0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera verde (o U) per la lettura dei dati di colore. Ad esempio, dato il formato A8R8G8B8, la maschera verde sarà 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera blu (o V) per la lettura dei dati di colore. Ad esempio, dato il formato A8R8G8B8, la maschera blu sarà 0x000000ff.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Maschera alfa per la lettura dei dati alfa. dwFlags deve includere *DDPF \_ ALPHAPIXELS* o *DDPF \_ ALPHA*. Ad esempio, dato il formato A8R8G8B8, la maschera alfa sarà 0xff000000.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per archiviare formati DXGI, ad esempio dati a virgola mobile, usare **dwFlags** di DDPF FOURCC e impostare \_ **dwFourCC** su 'D','X','1','0'. Usare [**l'intestazione \_ \_ dell'estensione DDS HEADER DXT10**](dds-header-dxt10.md) per archiviare il formato DXGI nel **membro dxgiFormat.**

Si noti che esistono varianti non standard dei file DDS in cui **dwFlags** ha DDPF FOURCC e il valore dwFourCC è impostato direttamente su un valore di enumerazione \_ D3DFORMAT o DXGI  \_ FORMAT. Non è possibile disambiguare i valori D3DFORMAT e DXGI FORMAT usando questo schema non standard, pertanto è consigliabile usare l'intestazione dell'estensione \_ DX10.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento per DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

