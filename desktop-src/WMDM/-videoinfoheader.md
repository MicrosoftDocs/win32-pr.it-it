---
title: _VIDEOINFOHEADER struttura
description: La struttura VIDEOINFOHEADER contiene informazioni su un flusso video e include una struttura BITMAPINFOHEADER che definisce il \_ formato di un singolo \_ frame.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER struttura windows Media Device Manager
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b00c641f0fb9a9f68217de8a21a732b4b45a8e4417104be981ffd90161f7340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586801"
---
# <a name="_videoinfoheader-structure"></a>\_Struttura VIDEOINFOHEADER

La **\_ struttura VIDEOINFOHEADER** contiene informazioni su un flusso video e include una **\_ struttura BITMAPINFOHEADER** che definisce il formato di un singolo frame.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**rcSource**
</dt> <dd>

**Struttura RECT** che specifica la finestra video di origine.

</dd> <dt>

**rcTarget**
</dt> <dd>

**Struttura RECT** che specifica la finestra video di destinazione.

</dd> <dt>

**dwBitRate**
</dt> <dd>

**Valore DWORD** che specifica la velocità approssimativa dei dati del flusso video, in bit al secondo.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

**Valore DWORD** che specifica la frequenza di errore dei dati del flusso video, in bit al secondo.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**INFORMAZIONI DI RIFERIMENTO \_ Valore** TIME che specifica il tempo di visualizzazione medio del fotogramma video, in unità da 100 nanosecondi.

</dd> <dt>

**bmiHeader**
</dt> <dd>

Struttura **\_ BITMAPINFOHEADER** Win32 che contiene informazioni sul colore e sulle dimensioni per la bitmap dell'immagine video.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





