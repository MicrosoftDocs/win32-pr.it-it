---
title: Proprietà WSMan.Error (WSManDisp.h)
description: Ottiene informazioni aggiuntive sull'errore, in un flusso XML, per la chiamata precedente a un metodo WSMan se Windows Servizio di gestione remota non è stato in grado di creare un oggetto Session, un oggetto ConnectionOptions o un oggetto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Proprietà Error Windows Remote Management
- Proprietà Error Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, proprietà Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d72c99150d3c6ac95e91e6a9674ab6364e8ea46fabf3d58d50556e129933cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742196"
---
# <a name="wsmanerror-property"></a>WSMan.Error - proprietà

Ottiene informazioni aggiuntive sull'errore, in un flusso XML, per la chiamata precedente a un metodo [**WSMan**](wsman.md) se Windows Servizio di gestione remota non è stato in grado di creare un oggetto [**Session,**](session.md) un oggetto [**ConnectionOptions**](connectionoptions.md) o [**un oggetto ResourceLocator.**](resourcelocator.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>Valore proprietà

Rappresentazione XML delle informazioni sull'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





