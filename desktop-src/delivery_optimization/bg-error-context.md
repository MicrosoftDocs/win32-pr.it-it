---
title: Enumerazione BG_ERROR_CONTEXT (Deliveryoptimization. h)
description: L'enumerazione BG_ERROR_CONTEXT definisce i valori costanti che specificano il contesto in cui si è verificato l'errore.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- Enumerazione BG_ERROR_CONTEXT
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476175"
---
# <a name="bg_error_context-enumeration"></a>Enumerazione BG_ERROR_CONTEXT

L'enumerazione **BG_ERROR_CONTEXT** definisce i valori costanti che specificano il contesto in cui si è verificato l'errore.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**
</dt> <dd>

Si è verificato un errore.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**
</dt> <dd>

Errore correlato al file remoto specificato. Ad esempio, l'URL non è accessibile.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**
</dt> <dd>

Non supportata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyError:: GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





