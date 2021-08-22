---
description: Esegue un'operazione di scambio di chiavi SSL (Server-Side Secure Sockets Layer Protocol).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Funzione SslImportMasterKey (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 546cfeb39ac413b99b5b8021dc7dd6f0f57a89dbfb87880a63b0db2324cda0d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906062"
---
# <a name="sslimportmasterkey-function"></a>Funzione SslImportMasterKey

La **funzione SslImportMasterKey** esegue un'operazione di scambio di chiavi SSL (Server-Side [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) Protocol).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per l'istanza del provider del protocollo SSL.

</dd> <dt>

*hPrivateKey* \[ Pollici\]
</dt> <dd>

Handle per la [*chiave privata utilizzata*](/windows/desktop/SecGloss/p-gly) nello scambio.

</dd> <dt>

*phMasterKey* \[ Cambio\]
</dt> <dd>

Puntatore all'handle per ricevere la [*chiave master*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwProtocol* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Protocol Identifier.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Cipher Suite Identifiers.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pParameterList* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni usate come parte dell'operazione di scambio delle chiavi. Il set preciso di buffer dipende dal protocollo e dalla suite di crittografia usata. Come minimo, l'elenco conterrà i buffer che contengono i valori casuali forniti dal client e dal server.

</dd> <dt>

*pbEncryptedKey* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer contenente la chiave privata premaster crittografata crittografata con la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) del server.

</dd> <dt>

*cbEncryptedKey* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbEncryptedKey.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Impostare questo parametro su **NCRYPT \_ SSL SERVER \_ \_ FLAG** per indicare che si tratta di una chiamata al server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno degli handle forniti non è valido.<br/>                     |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro phMasterKey* è **NULL.**<br/>                      |



 

## <a name="remarks"></a>Commenti

Questa funzione decrittografa il segreto premaster, calcola l'master secret SSL e restituisce un handle a questo oggetto al chiamante. Questa chiave master può quindi essere usata per derivare la chiave di sessione SSL e completare l'handshake SSL.

> [!Note]  
> Questa funzione viene usata quando viene usato [*l'algoritmo di*](/windows/desktop/SecGloss/r-gly) scambio di chiavi RSA. Quando [*si usa DH,*](/windows/desktop/SecGloss/d-gly) il codice server chiama [**invece SslGenerateMasterKey.**](sslgeneratemasterkey.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

