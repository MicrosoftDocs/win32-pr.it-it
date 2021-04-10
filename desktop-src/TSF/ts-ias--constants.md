---
title: Costanti TS_IAS_ (Textstor. h)
description: Le \_ costanti IAS \_ di Servizi terminal vengono utilizzate come flag bit per controllare l'inserimento di testo o di oggetti incorporati in una selezione o in un punto di inserimento.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119862"
---
# <a name="ts_ias_-constants"></a>\_Costanti IAS \_ di Servizi terminal \*

Le \_ costanti IAS di Servizi terminal \_ \* vengono utilizzate come flag bit per controllare l'inserimento di testo o oggetti incorporati in una selezione o in un punto di inserimento.



| Costante/valore                                                                                                                                                                                                                       | Descrizione                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <dt>**Servizi terminal \_ IAS \_ noquery**</dt> <dt>(0x1)</dt> </dl>       | Il testo viene inserito e il puntatore di intervallo è impostato su **null** all'uscita. Non può essere combinato con il \_ flag QUERYONLY IAS di Servizi terminal \_ .<br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <dt>**Servizi terminal \_ IAS \_ QUERYONLY**</dt> <dt>(0x2)</dt> </dl> | Non eseguire l'inserimento. Il chiamante richiede l'impostazione del puntatore di intervallo. Non possono essere combinati con \_ il \_ flag noquery IAS di Servizi terminal.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





