---
title: Proprietà Session.BatchItems (WSManDisp. h)
description: Imposta e ottiene il numero di elementi in ogni batch di enumerazione.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà BatchItems
- Gestione remota Windows proprietà BatchItems, oggetto Session
- Gestione remota Windows oggetto sessione, proprietà BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302329"
---
# <a name="sessionbatchitems-property"></a>Session.Batproprietà chItems

Imposta e ottiene il numero di elementi in ogni batch di enumerazione. Questo valore non può essere modificato durante un'enumerazione. Il provider di risorse può impostare un limite.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Valore proprietà

Specifica il numero massimo di elementi restituiti per ogni chiamata di rete sottostante al servizio. Il valore predefinito è 20.

## <a name="remarks"></a>Commenti

Si tratta di una funzionalità di ottimizzazione che controlla la frequenza con cui vengono effettuate chiamate di rete tra il client e il server. Attualmente, viene usato solo per le enumerazioni. Per ulteriori informazioni sull'enumerazione delle risorse [**, vedere Enumerazione**](session-enumerate.md).

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

[**Sessione**](session.md)
</dt> <dt>

[**Enumerazione**](session-enumerate.md)
</dt> <dt>

[**Enumeratore. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





