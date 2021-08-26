---
description: Il metodo get \_ ParticipantTypedInfo ottiene una rappresentazione BSTR del tipo di informazioni necessarie, ad esempio PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: Metodo ITParticipant::get_ParticipantTypedInfo (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43afb80b0f1161cf0060c8492576ade4f682af44cb4b2dbb13ab49d2c65aab66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867151"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>Metodo ITParticipant::get \_ ParticipantTypedInfo

\[**get \_ ParticipantTypedInfo** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ ParticipantTypedInfo** ottiene una **rappresentazione BSTR** del tipo di informazioni necessarie, ad esempio PTI \_ EMAILADDRESS.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ Pollici\]
</dt> <dd>

[**PARTECIPANTE \_ Descrittore \_ TYPED INFO**](participant-typed-info.md) del tipo di informazioni necessarie.

</dd> <dt>

*ppInfo* \[ Cambio\]
</dt> <dd>

Puntatore **alla rappresentazione BSTR** delle informazioni necessarie.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                    | Descrizione                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>         | Archiviazione di informazioni in *ppInfo non* riuscito.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il *parametro InfoType* non è valido.<br/>               |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>      | Il *parametro ppInfo* non è un puntatore valido.<br/>       |
| <dl> <dt>**TAPI \_ E \_ NOITEM**</dt> </dl> | TAPI non contiene informazioni sul tipo specificato.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il *parametro ppInfo.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**INFORMAZIONI \_ DIGITATE DAL \_ PARTECIPANTE**](participant-typed-info.md)
</dt> <dt>

[**tipi di supporti**](tapimediatype--constants.md)
</dt> </dl>

 

