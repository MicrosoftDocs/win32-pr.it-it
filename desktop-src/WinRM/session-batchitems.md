---
title: Session.Batproprietà chItems (WSManDisp.h)
description: Imposta e ottiene il numero di elementi in ogni batch di enumerazione.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Proprietà BatchItems Windows gestione remota
- Proprietà BatchItems Windows, oggetto Session di Gestione remota
- Oggetto Session Windows gestione remota, proprietà BatchItems
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
ms.openlocfilehash: 59e395eb27be2b922cf9d53e40f1d8cea0fc13a5dcf7b62b95ac606ec8f3f96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795341"
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

Si tratta di una funzionalità di ottimizzazione che controlla la frequenza con cui vengono effettuate chiamate di rete tra il client e il server. Attualmente, viene usato solo per le enumerazioni. Per altre informazioni sull'enumerazione delle risorse, vedere [**Enumerare**](session-enumerate.md).

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

[**Sessione**](session.md)
</dt> <dt>

[**Enumerazione**](session-enumerate.md)
</dt> <dt>

[**Enumerator.ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





