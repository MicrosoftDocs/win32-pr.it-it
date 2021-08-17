---
title: Costanti varie dell'archivio di testo (Textstor.h)
description: Le costanti dell'archivio di testo varie impostano determinate proprietà per gli archivi di testo.
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
ms.openlocfilehash: 55bfa06f7f0ebda1d572a4e637076de25c7a21ef4d273cdc2527ab6481393404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952099"
---
# <a name="miscellaneous-text-store-constants"></a>Costanti varie dell'archivio di testo

Le costanti dell'archivio di testo varie impostano determinate proprietà per gli archivi di testo.



| Costante/valore                                                                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ SELEZIONE \_ PREDEFINITA**</dt> <dt>( ( ULONG )-1 )</dt> </dl> | Se il *parametro ulIndex* di [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) è impostato su questo valore, viene ottenuta la selezione predefinita.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ GEA \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl>                              | Se *il parametro dwFlags* di [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) è impostato su questo valore, un oggetto incorporato può trovarsi all'interno del testo nascosto.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ GTA \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl>                              | Non usato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ ST \_ CORRECTION**</dt> <dt>( 0x1 )</dt> </dl>                     | Se il parametro *dwFlags* di [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)o [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) è impostato su questo valore, il testo è una trasformazione (correzione) del contenuto esistente e vengono mantenute eventuali informazioni speciali di markup del testo (metadati), ad esempio dati di file wav o un identificatore di lingua.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ CORREZIONE \_ TC**</dt> <dt>( 0x1 )</dt> </dl>                     | Se il parametro *dwFlags* di [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) è impostato su questo valore, il testo è una trasformazione (correzione) del contenuto esistente e tutte le informazioni speciali sul markup del testo (metadati) vengono mantenute, ad esempio i dati del file wav o un identificatore di lingua.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ VCOOKIE \_ NUL**</dt> <dt>( 0xffffffff )</dt> </dl>                    | Usato internamente da TSF.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Costanti varie del framework](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





