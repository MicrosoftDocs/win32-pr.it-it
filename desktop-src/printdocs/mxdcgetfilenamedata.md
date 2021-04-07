---
description: La \_ struttura MXDC Get \_ filename \_ data \_ T include il percorso completo e il nome file di un file di output di Microsoft XPS Document Converter (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Struttura MXDC_GET_FILENAME_DATA_T (MXDC. h)
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
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881606"
---
# <a name="mxdc_get_filename_data_t-structure"></a>MXDC \_ ottenere \_ la \_ struttura dei dati filename \_

La struttura **MXDC \_ get \_ filename \_ data \_ T** include il percorso completo e il nome file di un file di output di Microsoft XPS Document Converter (MXDC).

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

Questa struttura viene restituita da [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape di escape [**MXDC \_**](mxdc-escape.md) e la struttura dell' [**intestazione di \_ escape \_ \_ MXDC**](mxdcescapeheader.md) che viene passata nel parametro *lpszInData* è impostata sul **codice operativo** **MXDCOP \_ get \_ filename**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>MXDC. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**\_escape MXDC**](mxdc-escape.md)
</dt> </dl>

 

