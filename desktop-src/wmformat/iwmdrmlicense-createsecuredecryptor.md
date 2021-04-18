---
title: Metodo IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: Il metodo CreateSecureDecryptor crea un oggetto di decrittografia protetto. Il decrittografia sicuro è diverso da quello normale in quanto decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Metodo CreateSecureDecryptor Windows Media Format
- Metodo CreateSecureDecryptor Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo CreateSecureDecryptor
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
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324283"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>Metodo IWMDRMLicense:: CreateSecureDecryptor

Il metodo **CreateSecureDecryptor** crea un oggetto di decrittografia protetto. Il decrittografia sicuro è diverso da quello normale in quanto decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.

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

*pbCertificate* \[ in\]
</dt> <dd>

Certificato dell'applicazione chiamante.

</dd> <dt>

*cbCertificate* \[ in\]
</dt> <dd>

Dimensioni in byte del certificato.

</dd> <dt>

*dwCertificateType* \[ in\]
</dt> <dd>

Tipo di certificato. Impostare sul \_ tipo di certificato WMDRM \_ \_ XML.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Tipo di protezione della sessione da utilizzare per la nuova codifica. Deve essere impostato su una delle costanti della tabella seguente:



| Costante                     | Descrizione                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| \_Tipo di protezione WMDRM \_ \_ RC4 | Usa la crittografia RC4 per la crittografia della sessione. Questa è l'unica protezione della sessione supportata per questa versione. |



 

</dd> <dt>

*pbInitializationVector* \[ out\]
</dt> <dd>

Riceve il vettore di inizializzazione. Il vettore di inizializzazione è crittografato con RSA usando lo schema di riempimento OAEP con la chiave pubblica RSA trovata nel certificato. Impostare su **null** per ricevere le dimensioni del buffer richieste in *pcbInitializationVector*.

</dd> <dt>

*pcbInitializationVector* \[ in uscita\]
</dt> <dd>

In input, dimensione del buffer passata come *pbInitializationVector*. Nell'output, dimensioni della parte utilizzata del buffer. Se si passa **null** per *pbInitializationVector*, questo valore viene impostato sulla dimensione del buffer richiesta nell'output.

</dd> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





