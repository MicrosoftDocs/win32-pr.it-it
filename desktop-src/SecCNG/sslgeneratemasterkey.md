---
description: Calcola la chiave di master secret SSL (Secure Sockets Layer Protocol).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Funzione SslGenerateMasterKey (Sslprovider. h)
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
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401802"
---
# <a name="sslgeneratemasterkey-function"></a>SslGenerateMasterKey (funzione)

La funzione **SslGenerateMasterKey** calcola la chiave di master secret SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider del protocollo SSL.

</dd> <dt>

*hPrivateKey* \[ in\]
</dt> <dd>

Handle per la [*chiave privata*](/windows/desktop/SecGloss/p-gly) utilizzata in Exchange.

</dd> <dt>

*hPublicKey* \[ in\]
</dt> <dd>

Handle per la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) utilizzata in Exchange.

</dd> <dt>

*phMasterKey* \[ out\]
</dt> <dd>

Puntatore all'handle per la [*chiave master*](/windows/desktop/SecGloss/m-gly)generata.

</dd> <dt>

*dwProtocol* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ in\]
</dt> <dd>

Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni utilizzate come parte dell'operazione di scambio delle chiavi. Il set preciso di buffer dipende dal protocollo e dal pacchetto di crittografia utilizzati. Come minimo, l'elenco conterrà i buffer contenenti i valori casuali specificati dal client e dal server.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Indirizzo di un buffer che riceve il segreto premaster crittografato con la chiave pubblica del server. Il parametro *cbOutput* contiene la dimensione del buffer. Se questo parametro è **null**, questa funzione restituisce la dimensione richiesta, in byte, nel **valore DWORD** a cui punta il parametro *pcbResult* .

> [!Note]  
> Questo buffer viene usato quando si esegue uno scambio di chiavi RSA.

 

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

Puntatore a un valore **DWORD** in cui inserire il numero di byte scritti nel buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Specifica se questa funzione viene utilizzata per lo scambio di chiavi sul lato client o sul lato server.



| Valore                                                                                                                                                                                                                                                      | Significato                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Flag client SSL**</dt> <dt>0x00000001</dt> </dl> | Specifica uno scambio di chiavi sul lato client.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Flag server SSL**</dt> <dt>0x00000002</dt> </dl> | Specifica uno scambio di chiavi sul lato server.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | La memoria disponibile non è sufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Uno degli handle forniti non è valido.<br/>                     |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *phMasterKey* o *hPublicKey* non è valido.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

