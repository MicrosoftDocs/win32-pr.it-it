---
title: Costanti TF_SD_ (msctf. h)
description: Le \_ costanti TF SD \_ \ descrivono lo stato del documento.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119119"
---
# <a name="tf_sd_-constants"></a>\_Costanti SD \_ \* TF

Le \_ costanti SD TF \_ \* descrivono lo stato del documento.



| Costante/valore                                                                                                                                                                                                                              | Descrizione                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**Tf \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt> </dl> | Il documento è di sola lettura e non può essere modificato.<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**Tf \_ \_caricamento SD**</dt> <dt>( \_ caricamento SD TS \_ )</dt> </dl>     | Il documento viene caricato e può essere incompleto.<br/>    |



## <a name="remarks"></a>Commenti

Il membro **dwDynamicFlags** della struttura [di \_ stato TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) usa queste costanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_stato TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[\_Costanti SD \_ \* TS](ts-sd--constants.md)
</dt> <dt>

[ITfContextOwner:: GetStatus](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[ITfContextOwnerServices:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP:: GetStatus](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[ITfStatusSunk:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

