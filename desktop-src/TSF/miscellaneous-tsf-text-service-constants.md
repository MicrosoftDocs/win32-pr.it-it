---
title: Costanti varie del servizio di testo TSF (Ctffunc.h)
description: I valori seguenti vengono usati con i servizi di testo.
ms.assetid: 38110314-1638-4963-92b6-4ba2f81fb7c2
topic_type:
- apiref
api_name:
- TF_MENUREADY
- TF_PROPUI_STATUS_SAVETOFILE
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd4d9cdd73cd42512fe667b84867328c65f13fafa7281341eca7ba6379eef7d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476771"
---
# <a name="miscellaneous-tsf-text-service-constants"></a>Costanti varie del servizio di testo TSF

I valori seguenti vengono usati con i servizi di testo.



| Costante/valore                                                                                                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <dt>**TF \_ MENUREADY**</dt> <dt>0x00000001</dt> </dl>                                                | Attualmente non utilizzato.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <dt>**TF \_ STATO \_ PROPUI \_ SAVETOFILE**</dt> <dt>0x00000001</dt> </dl> | La proprietà può essere serializzata. Se questo valore non è presente, la proprietà non può essere serializzata. Questo valore viene usato con [ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) e [ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1.0 in Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Ctffunc.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITfFnPropertyUIStatus::GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[ITfFnPropertyUIStatus::SetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





