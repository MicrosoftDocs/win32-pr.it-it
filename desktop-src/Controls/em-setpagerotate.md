---
title: Messaggio di EM_SETPAGEROTATE (RichEdit. h)
description: Imposta il layout del testo per un controllo Rich Edit.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- Controlli di Windows Message EM_SETPAGEROTATE
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964119"
---
# <a name="em_setpagerotate-message"></a>\_Messaggio SETPAGEROTATE em

\[**Em \_ SETPAGEROTATE** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Imposta il layout del testo per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore del layout del testo. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                       | Significato                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <dt>**EPR \_ 0**</dt> </dl>       | Il testo scorre da sinistra verso destra e dall'alto verso il basso.<br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <dt>**EPR \_ 90**</dt> </dl>    | Il testo scorre dal basso verso l'alto e da sinistra a destra.<br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <dt>**EPR \_ 180**</dt> </dl> | Il testo scorre da destra a sinistra e dal basso verso l'alto.<br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <dt>**EPR \_ 270**</dt> </dl> | Il testo scorre dall'alto verso il basso e da destra a sinistra.<br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <dt>**EPR \_ se**</dt> </dl>    | **Windows 8:** Il testo scorre dall'alto verso il basso e da sinistra verso destra (layout di testo mongolo).<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il nuovo valore del layout del testo.

## <a name="remarks"></a>Commenti

Questo messaggio consente di impostare il layout del testo per l'intero documento. Tuttavia, il contenuto incorporato non viene ruotato e deve essere ruotato separatamente dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETPAGEROTATE em**](em-getpagerotate.md)
</dt> </dl>

 

 





