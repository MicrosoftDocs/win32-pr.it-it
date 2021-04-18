---
title: Costanti TS_SD_ (Textstor. h)
description: Le \_ costanti SD \_ \ ts descrivono gli Stati dei documenti dinamici usati da un'applicazione in fase di esecuzione.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301344"
---
# <a name="ts_sd_-constants"></a>\_Costanti SD \_ \* TS

Le \_ costanti SD TS \_ \* descrivono gli Stati dei documenti dinamici usati da un'applicazione in fase di esecuzione.



| Costante/valore                                                                                                                                                                                                                                              | Descrizione                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <dt>**Servizi terminal \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt> </dl>                              | Il documento è di sola lettura e non può essere modificato.<br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <dt>**Servizi terminal \_ \_Caricamento SD**</dt> <dt>(0x2)</dt> </dl>                                 | Il documento viene caricato e potrebbe essere incompleto.<br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <dt>**Servizi terminal \_ SD \_ MASKALL**</dt> <dt>( \_ \_ \| \_ \_ caricamento SD TS SD ReadOnly)</dt> </dl> | Il documento è di sola lettura e viene caricato.<br/>       |



## <a name="remarks"></a>Commenti

Il membro **dwDynamicFlags** della struttura [di \_ stato TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) usa queste costanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[stato di Servizi terminal \_](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[\_Costanti SD \_ \* TF](tf-sd--constants.md)
</dt> </dl>

 

 





