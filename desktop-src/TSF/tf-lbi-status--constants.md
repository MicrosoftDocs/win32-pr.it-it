---
title: Costanti TF_LBI_STATUS_ (Ctfutb. h)
description: Le \_ costanti TF LBI \_ status \_ \ indicano lo stato di un elemento della barra della lingua. Questi valori vengono usati con il metodo ITfLangBarItem GetStatus.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742922"
---
# <a name="tf_lbi_status_-constants"></a>\_Costanti di \_ stato TF LBI \_ \*

Le costanti ** \_ tf \_ LBI \_ \* status* _ indicano lo stato di un elemento della barra della lingua. Questi valori vengono usati con il metodo [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .



| Costante/valore                                                                                                                                                                                                                                                       | Descrizione                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>_ * TF \_ \_Stato LBI \_ nascosto * *</dt> <dt>0x00000001</dt> </dl>                 | L'elemento è nascosto. Questo stile viene ignorato se l'elemento non include lo stile HIDDENSTATUSCONTROL di TF \_ LBI \_ Style \_ .<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**Tf \_ \_Stato LBI \_ disabilitato**</dt> <dt>0x00000002</dt> </dl>           | L'elemento è disabilitato.<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**Tf \_ LBI \_ stato \_ BTN \_ attivato/disattivato**</dt> <dt>0x00010000</dt> </dl> | L'elemento è nello stato attivato o disattivato. Questo stile viene ignorato se l'elemento non include lo stile di \_ \_ interruttore BTN stile TF LBI \_ \_ .<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





