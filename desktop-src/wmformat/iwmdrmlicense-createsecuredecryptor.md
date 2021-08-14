---
title: Metodo IWMDRMLicense CreateSecureDecryptor (Wmdrmsdk.h)
description: Il metodo CreateSecureDecryptor crea un oggetto di decrittografia sicuro. Il componente di decrittografia sicura differisce dal normale componente di decrittografia perché decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Metodo CreateSecureDecryptor windows Media Format
- Metodo CreateSecureDecryptor windows Media Format , interfaccia IWMDRMLicense
- Metodo CreateSecureDecryptor dell'interfaccia IWMDRMLicense per Windows Media Format
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c562dcafd72a72ecef340688fd709ecbe5446abae53403d403c9a70bdd6f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433670"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>Metodo IWMDRMLicense::CreateSecureDecryptor

Il **metodo CreateSecureDecryptor** crea un oggetto di decrittografia sicuro. Il componente di decrittografia sicura differisce dal normale componente di decrittografia perché decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbCertificate* \[ Pollici\]
</dt> <dd>

Certificato dell'applicazione chiamante.

</dd> <dt>

*cbCertificate* \[ Pollici\]
</dt> <dd>

Dimensioni del certificato in byte.

</dd> <dt>

*dwCertificateType* \[ Pollici\]
</dt> <dd>

Tipo di certificato. Impostare su WMDRM \_ CERTIFICATE \_ TYPE XML(XML TIPO DI \_ CERTIFICATO WMDRM).

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Tipo di protezione della sessione da usare per la ri codifiche. Deve essere impostato su una delle costanti nella tabella seguente:



| Costante                     | Descrizione                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| WMDRM \_ PROTECTION \_ TYPE \_ RC4 | Usa la crittografia RC4 per la crittografia della sessione. Questa è l'unica protezione di sessione supportata per questa versione. |



 

</dd> <dt>

*pbInitializationVector* \[ Cambio\]
</dt> <dd>

Riceve il vettore di inizializzazione. Il vettore di inizializzazione viene crittografato con RSA usando lo schema di riempimento OAEP con la chiave pubblica RSA presente nel certificato. Impostare su **NULL per** ricevere le dimensioni del buffer richieste in *pcbInitializationVector.*

</dd> <dt>

*pcbInitializationVector* \[ in, out\]
</dt> <dd>

Nell'input, la dimensione del buffer passata *come pbInitializationVector*. Nell'output, la dimensione della parte usata del buffer. Se si passa **NULL per** *pbInitializationVector*, questo valore viene impostato sulle dimensioni del buffer richieste nell'output.

</dd> <dt>

*ppDecryptor* \[ Cambio\]
</dt> <dd>

Riceve un puntatore [**all'interfaccia IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





