---
description: La struttura MXDC GET FILENAME DATA T contiene il percorso completo e il nome file di un file di \_ \_ output di Microsoft \_ \_ XPS Document Converter (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: MXDC_GET_FILENAME_DATA_T (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ef0b29590b4a9080e943fae5c3e78fb18a99232a2a531a80b63b303b28c2bea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948341"
---
# <a name="mxdc_get_filename_data_t-structure"></a>Struttura MXDC \_ GET \_ FILENAME DATA \_ \_ T

La **struttura MXDC \_ GET FILENAME \_ DATA \_ \_ T** contiene il percorso completo e il nome file di un file di output di Microsoft XPS Document Converter (MXDC).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Members

<dl> <dt>

**cbOutput**
</dt> <dd>

Dimensioni del buffer di output, **wszData**.

</dd> <dt>

**wszData**
</dt> <dd>

Percorso completo e nome file del file di output.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene restituita da [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape [**\_ ESCAPE MXDC**](mxdc-escape.md) e la struttura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) passata nel parametro *lpszInData* ha il relativo **opCode** impostato su **MXDCOP \_ GET \_ FILENAME**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

