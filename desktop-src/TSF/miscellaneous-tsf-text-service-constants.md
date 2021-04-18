---
title: Costanti del servizio di testo TSF varie (Ctffunc. h)
description: Con i servizi di testo vengono usati i valori seguenti.
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
ms.openlocfilehash: d7ebd7d22f9cfbd59f95ee3dcfe68229536503b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302245"
---
# <a name="miscellaneous-tsf-text-service-constants"></a>Costanti del servizio di testo TSF varie

Con i servizi di testo vengono usati i valori seguenti.



| Costante/valore                                                                                                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MENUREADY"></span><span id="tf_menuready"></span><dl> <dt>**Tf \_**</dt> <dt>0x00000001</dt> MENUREADY </dl>                                                | Attualmente non utilizzato.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_PROPUI_STATUS_SAVETOFILE"></span><span id="tf_propui_status_savetofile"></span><dl> <dt>**Tf \_ PROPUI \_ stato \_ SAVETOFILE**</dt> <dt>0x00000001</dt> </dl> | La proprietà può essere serializzata. Se questo valore non è presente, la proprietà non può essere serializzata. Questo valore viene usato con [ITfFnPropertyUIStatus:: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus) e [ITfFnPropertyUIStatus:: sestatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus).<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITfFnPropertyUIStatus:: GetStatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-getstatus)
</dt> <dt>

[ITfFnPropertyUIStatus:: sestatus](/windows/desktop/api/Ctffunc/nf-ctffunc-itffnpropertyuistatus-setstatus)
</dt> </dl>

 

 





