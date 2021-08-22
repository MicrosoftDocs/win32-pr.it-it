---
description: Calcola la chiave Secure Sockets Layer (SSL) master secret chiave.
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Funzione SslGenerateMasterKey (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4e1ca35493667cb6e7e3d5ba8b162a3d073d51fc397ce2e1a1da7ab7a380728d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906254"
---
# <a name="sslgeneratemasterkey-function"></a>Funzione SslGenerateMasterKey

La **funzione SslGenerateMasterKey** calcola la [*chiave Secure Sockets Layer (SSL)*](/windows/desktop/SecGloss/s-gly) master secret chiave.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
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

Handle per la [*chiave privata*](/windows/desktop/SecGloss/p-gly) utilizzata nello scambio.

</dd> <dt>

*hPublicKey* \[ Pollici\]
</dt> <dd>

Handle per la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) utilizzata nello scambio.

</dd> <dt>

*phMasterKey* \[ Cambio\]
</dt> <dd>

Puntatore all'handle per la chiave [*master generata.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*dwProtocol* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Protocol Identifier.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Cipher Suite Identifier.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*pParameterList* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni usate come parte dell'operazione di scambio delle chiavi. Il set preciso di buffer dipende dal protocollo e dalla suite di crittografia usati. Come minimo, l'elenco conterrà i buffer che contengono i valori casuali forniti dal client e dal server.

</dd> <dt>

*pbOutput* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer che riceve il segreto premaster crittografato con la chiave pubblica del server. Il *parametro cbOutput* contiene le dimensioni di questo buffer. Se questo parametro è **NULL,** questa funzione restituisce le dimensioni richieste, in byte, nel **valore DWORD** a cui punta *il parametro pcbResult.*

> [!Note]  
> Questo buffer viene usato quando si esegue uno scambio di chiavi RSA.

 

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput.*

</dd> <dt>

*pcbResult* \[ Cambio\]
</dt> <dd>

Puntatore a un **valore DWORD** in cui inserire il numero di byte scritti nel buffer *pbOutput.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Specifica se questa funzione viene utilizzata per lo scambio di chiavi sul lato client o sul lato server.



| Valore                                                                                                                                                                                                                                                      | Significato                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ Flag \_ \_ CLIENT SSL**</dt> <dt>0x00000001</dt> </dl> | Specifica uno scambio di chiavi sul lato client.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ Flag \_ \_ DEL SERVER SSL**</dt> <dt>0x00000002</dt> </dl> | Specifica uno scambio di chiavi lato server.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno degli handle forniti non è valido.<br/>                     |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro phMasterKey* *o hPublicKey* non è valido.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

