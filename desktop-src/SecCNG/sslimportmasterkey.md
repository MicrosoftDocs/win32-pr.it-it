---
description: Esegue un'operazione di scambio di chiave del protocollo SSL (Secure Sockets Layer) sul lato server.
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Funzione SslImportMasterKey (Sslprovider. h)
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
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311937"
---
# <a name="sslimportmasterkey-function"></a>SslImportMasterKey (funzione)

La funzione **SslImportMasterKey** esegue un'operazione di scambio di chiave del protocollo SSL ( [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) ) sul lato server.

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider del protocollo SSL.

</dd> <dt>

*hPrivateKey* \[ in\]
</dt> <dd>

Handle per la [*chiave privata*](/windows/desktop/SecGloss/p-gly) utilizzata in Exchange.

</dd> <dt>

*phMasterKey* \[ out\]
</dt> <dd>

Puntatore all'handle per la ricezione della [*chiave master*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwProtocol* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ in\]
</dt> <dd>

Uno dei valori degli [**identificatori del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ in\]
</dt> <dd>

Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni utilizzate come parte dell'operazione di scambio delle chiavi. Il set preciso di buffer dipende dal protocollo e dal pacchetto di crittografia utilizzati. Come minimo, l'elenco conterrà i buffer contenenti i valori casuali specificati dal client e dal server.

</dd> <dt>

*pbEncryptedKey* \[ in\]
</dt> <dd>

Puntatore a un buffer contenente la chiave privata premaster crittografata crittografata con la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) del server.

</dd> <dt>

*cbEncryptedKey* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbEncryptedKey* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Impostare questo parametro su **NCRYPT \_ SSL \_ server \_ flag** per indicare che si tratta di una chiamata al server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | La memoria disponibile non è sufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Uno degli handle forniti non è valido.<br/>                     |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *phMasterKey* è **null**.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questa funzione decrittografa il segreto premaster, calcola il master secret SSL e restituisce al chiamante un handle per questo oggetto. Questa chiave master può quindi essere usata per derivare la chiave di sessione SSL e completare l'handshake SSL.

> [!Note]  
> Questa funzione viene usata quando si usa l'algoritmo di scambio delle chiavi [*RSA*](/windows/desktop/SecGloss/r-gly) . Quando si usa [*DH*](/windows/desktop/SecGloss/d-gly) , il codice server chiama invece [**SslGenerateMasterKey**](sslgeneratemasterkey.md) .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

