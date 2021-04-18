---
description: Il metodo SetDefaultClassId assegna un byte dell'identificatore di classe standard che verrà usato in tutte le operazioni quando si costruisce un'unità dati del protocollo ISO 7816-4 (APDU). Per impostazione predefinita, il byte dell'identificatore di classe standard è 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'Metodo ISCardISO7816:: SetDefaultClassId (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313739"
---
# <a name="iscardiso7816setdefaultclassid-method"></a>Metodo ISCardISO7816:: SetDefaultClassId

\[Il metodo **SetDefaultClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **SetDefaultClassId** assegna un byte dell'identificatore di classe standard che verrà usato in tutte le operazioni quando si costruisce un' [*unità dati del protocollo*](../secgloss/a-gly.md) ISO 7816-4 (APDU). Per impostazione predefinita, il byte dell'identificatore di classe standard è 0x00.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byClass* \[ in\]
</dt> <dd>

Byte ID classe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

I possibili valori restituiti sono i seguenti:



| Codice restituito                                                                          | Descrizione                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Operazione completata correttamente.<br/> |



 

Per un elenco di tutti i metodi forniti dall'interfaccia [**ISCardISO7816**](iscardiso7816.md) , vedere **ISCardISO7816**.

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
