---
description: Il metodo get \_ Description ottiene la descrizione della sessione (BSTR).
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: Metodo ITSdp::get_Description (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5466200a3efe51e102af5bb2abb92e86dff5c49a10f3f6498c77a992ba43073d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945047"
---
# <a name="itsdpget_description-method"></a>Metodo ITSdp::get \_ Description

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ Description** ottiene la descrizione della sessione (**BSTR**). Deve essere una stringa convertibile ASCII se il set di caratteri è ASCII. In caso contrario, può essere qualsiasi **stringa BSTR.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDescription* \[ Cambio\]
</dt> <dd>

Puntatore a un **BSTR contenente** la descrizione della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro ppDescription* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                   |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare il *parametro ppDescription.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**Descrizione di ITSdp::p ut \_**](itsdp-put-description.md)
</dt> </dl>

 

