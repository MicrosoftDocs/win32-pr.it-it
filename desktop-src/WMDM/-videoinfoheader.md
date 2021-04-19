---
title: Struttura _VIDEOINFOHEADER
description: La \_ struttura VIDEOINFOHEADER contiene informazioni su un flusso video e include una \_ struttura BITMAPINFOHEADER che definisce il formato di un singolo frame.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Struttura di _VIDEOINFOHEADER Windows Media Gestione dispositivi
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
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324227"
---
# <a name="_videoinfoheader-structure"></a>\_Struttura VIDEOINFOHEADER

La struttura **\_ VIDEOINFOHEADER** contiene informazioni su un flusso video e include una struttura **\_ BITMAPINFOHEADER** che definisce il formato di un singolo frame.

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

Struttura **Rect** che specifica la finestra del video di origine.

</dd> <dt>

**rcTarget**
</dt> <dd>

Struttura **Rect** che specifica la finestra video di destinazione.

</dd> <dt>

**dwBitRate**
</dt> <dd>

Valore **DWORD** che specifica la velocità dati approssimativa del flusso video, in bit al secondo.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

Valore **DWORD** che specifica la frequenza di errore dei dati del flusso video, in errori di bit al secondo.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

Informazioni di **riferimento \_** Valore di ora che specifica il tempo medio di visualizzazione del fotogramma video, in unità di 100 nanosecondi.

</dd> <dt>

**bmiHeader**
</dt> <dd>

Struttura **\_ BITMAPINFOHEADER** Win32 che contiene le informazioni relative al colore e alla dimensione per la bitmap dell'immagine video.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





