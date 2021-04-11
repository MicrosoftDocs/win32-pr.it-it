---
title: Proprietà WSMan. Error (WSManDisp. h)
description: Ottiene informazioni aggiuntive sull'errore, in un flusso XML, per la chiamata precedente a un metodo WSMan se Gestione remota Windows servizio non è stato in grado di creare un oggetto sessione, un oggetto ConnectionOptions o un oggetto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà errore
- Gestione remota Windows proprietà errore, oggetto WSMan
- Gestione remota Windows oggetto WSMan, proprietà Error
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
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119854"
---
# <a name="wsmanerror-property"></a>WSMan. Error (proprietà)

Ottiene informazioni aggiuntive sull'errore, in un flusso XML, per la chiamata precedente a un metodo [**WSMan**](wsman.md) se gestione remota Windows servizio non è stato in grado di creare un oggetto [**sessione**](session.md) , un oggetto [**ConnectionOptions**](connectionoptions.md) o un oggetto [**resourceLocator**](resourcelocator.md) .

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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





