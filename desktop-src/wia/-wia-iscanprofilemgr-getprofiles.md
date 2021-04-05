---
description: Ottiene tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Metodo IScanProfileMgr:: GetProfiles (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756644"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>Metodo IScanProfileMgr:: GetProfiles

Ottiene tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pulNumProfiles* \[ in uscita\]
</dt> <dd>

Tipo: **ULONG \** _

Quando viene passato, un puntatore al numero massimo di profili da restituire. Quando viene restituito, un puntatore al numero di profili restituiti.

</dd> <dt>

_ppScanProfile * \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Indirizzo di una matrice di puntatori ai profili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il numero totale di profili disponibili per l'utente è inferiore al valore passato a *pulNumProfiles*, *pulNumProfiles* restituisce il totale. In caso contrario, restituisce lo stesso valore che è stato passato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




