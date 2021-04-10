---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: Il formato degli Appunti dell'elenco di selezione di CFSTR \_ DSOP \_ DS \_ \_ fornisce un HGLOBAL che contiene una \_ struttura di elenco di selezione DS \_ . La \_ struttura dell'elenco di selezione DS contiene i \_ dati relativi agli elementi selezionati in una finestra di dialogo di selezione oggetti directory.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964059"
---
# <a name="cfstr_dsop_ds_selection_list"></a>\_elenco di \_ \_ selezione DS DSOP CFSTR \_

<dl> <dt>

<span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**\_elenco di \_ \_ selezione DS DSOP CFSTR \_**
</dt> <dd> <dl> <dt>

"CFSTR \_ DSOP \_ DS \_ Selection \_ List"
</dt> <dt>



Il formato degli Appunti dell' **elenco di \_ selezione CFSTR DSOP \_ DS \_ \_** viene fornito dal [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ottenuto chiamando [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog). Il formato degli Appunti dell' **elenco di selezione di CFSTR \_ DSOP \_ \_ \_ DS** fornisce un **HGLOBAL** che contiene una struttura di [**\_ \_ elenco di selezione DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . La struttura dell' **\_ \_ elenco di selezione DS** contiene i dati relativi agli elementi selezionati in una finestra di dialogo di [selezione oggetti directory](directory-object-picker.md) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Objsel. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_elenco di selezione DS \_**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[Selezione oggetti directory](directory-object-picker.md)
</dt> </dl>

 

