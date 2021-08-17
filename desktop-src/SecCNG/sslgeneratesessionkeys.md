---
description: Genera un set di Secure Sockets Layer di sessione SSL (Secure Sockets Layer Protocol).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Funzione SslGenerateSessionKeys (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3a9d7a25e5dd2035bd0b060ae11904e351489309b3a5e3c65c0e1582dce77500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906173"
---
# <a name="sslgeneratesessionkeys-function"></a>Funzione SslGenerateSessionKeys

La **funzione SslGenerateSessionKeys** genera un set [*di chiavi Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) di sessione SSL (Secure Sockets Layer Protocol).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per l'istanza del provider del protocollo SSL.

</dd> <dt>

*hMasterKey* \[ Pollici\]
</dt> <dd>

Handle per [*l'oggetto chiave master.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*phReadKey* \[ Cambio\]
</dt> <dd>

Puntatore all'handle della chiave di lettura restituito.

</dd> <dt>

*phWriteKey* \[ Cambio\]
</dt> <dd>

Puntatore all'handle della chiave di scrittura restituito.

</dd> <dt>

*pParameterList* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni usate come parte dell'operazione di scambio delle chiavi. Il set preciso di buffer dipende dal protocollo e dalla suite di crittografia usati. Come minimo, l'elenco conterrà i buffer che contengono i valori casuali forniti dal client e dal server.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno degli handle forniti non è valido.<br/>                     |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON**</dt> <dt>VALIDO 0x80090027L</dt> </dl> | Il *parametro phReadKey* *o phWriteKey* è Null.<br/>            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

