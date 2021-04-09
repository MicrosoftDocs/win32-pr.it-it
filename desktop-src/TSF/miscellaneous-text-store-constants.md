---
title: Costanti di archivio di testo varie (Textstor. h)
description: Le costanti di archivio di testo varie impostano determinate proprietà per gli archivi di testo.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120918"
---
# <a name="miscellaneous-text-store-constants"></a>Costanti di archivio di testo varie

Le costanti di archivio di testo varie impostano determinate proprietà per gli archivi di testo.



| Costante/valore                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**Servizi terminal \_ \_Selezione predefinita**</dt> <dt>((ulong)-1)</dt> </dl> | Se il parametro *ulIndex* di [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) è impostato su questo valore, viene ottenuta la selezione predefinita.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**Servizi terminal \_ GEA \_ Hidden**</dt> <dt>(0x1)</dt> </dl>                              | Se il parametro *dwFlags* di [ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) è impostato su questo valore, un oggetto incorporato può trovarsi all'interno di un testo nascosto.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**Servizi terminal \_ GTA \_ nascosto**</dt> <dt>(0x1)</dt> </dl>                              | Non usato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**Servizi terminal \_ \_Correzione St**</dt> <dt>(0x1)</dt> </dl>                     | Se il parametro *dwFlags* di [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)o [ITextStoreACPSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) è impostato su questo valore, il testo è una trasformazione (correzione) del contenuto esistente e vengono mantenute le informazioni di markup (metadati) speciali, ad esempio i dati del file con estensione wav o un identificatore di lingua.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**Servizi terminal \_ \_Correzione TC**</dt> <dt>(0x1)</dt> </dl>                     | Se il parametro *dwFlags* di [ITextStoreAnchorSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) è impostato su questo valore, il testo è una trasformazione (correzione) del contenuto esistente e vengono mantenute le informazioni di markup (metadati) speciali, ad esempio i dati del file WAV o un identificatore di lingua.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**Servizi terminal \_ VCOOKIE \_ NUL**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                    | Utilizzato internamente da TSF.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



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

[ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Costanti del Framework varie](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





