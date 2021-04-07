---
description: Ottiene la chiave utilizzata per crittografare i messaggi in uscita protetti dal token.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'Metodo IUpdateEndpointAuthToken:: SigningKey (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049541"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a>Metodo IUpdateEndpointAuthToken:: SigningKey

Ottiene la chiave utilizzata per crittografare i messaggi in uscita protetti dal token.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbKey* \[ in uscita\]
</dt> <dd>

Chiave utilizzata per crittografare il messaggio in uscita.

</dd> <dt>

*pcbKeySize* \[ in uscita\]
</dt> <dd>

Dimensione della chiave a cui fa riferimento il rndSrc *pbkey* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se ha esito positivo. In caso contrario, restituisce un codice di errore COM o Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




