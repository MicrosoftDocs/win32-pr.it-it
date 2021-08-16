---
description: Copia il contenuto di un archivio certificati aperto in una stringa codificata.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Metodo Store.Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9adf0f42d64e0bc7ced76441ae0fe1da2d2b6609d9d717d5e3b26f8dd07db7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897806"
---
# <a name="storeexport-method"></a>Metodo Store.Export

\[Il **metodo** Export è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Export** copia il contenuto di un archivio certificati [*aperto*](../secgloss/c-gly.md) in una stringa codificata.

## <a name="syntax"></a>Sintassi


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SaveAs* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione [CAPICOM \_ STORE SAVE AS \_ \_ \_ TYPE](capicom-store-save-as-type.md) che indica il formato per l'operazione di esportazione. Il valore predefinito è CAPICOM \_ STORE \_ SAVE AS \_ \_ SERIALIZED. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                     | Significato                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**SALVATAGGIO \_ DELL'ARCHIVIO CAPICOM \_ COME \_ \_ SERIALIZZATO**</dt> </dl> | L'archivio viene salvato in formato serializzato.<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**CAPICOM STORE SAVE AS PKCS7 (SALVA ARCHIVIO CAPICOM \_ \_ COME \_ \_ PKCS7)**</dt> </dl>                | L'archivio viene salvato in formato PKCS \# 7.<br/>   |



 

</dd> <dt>

*Tipo di codifica* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione [CAPICOM \_ ENCODING \_ TYPE](capicom-encoding-type.md) che indica il tipo di codifica dell'archivio esportato. Il valore predefinito è CAPICOM \_ ENCODE \_ BASE64. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                  | Significato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Questo tipo di codifica viene usato solo quando i dati di input hanno un tipo di codifica sconosciuto. Se questo valore viene usato per specificare il tipo di codifica dell'output, verrà usato CAPICOM \_ ENCODE \_ BASE64. Introdotto in CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BASE64**</dt> </dl> | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BINARY**</dt> </dl> | I dati vengono salvati come sequenza binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una stringa che contiene i certificati nell'archivio nel formato di codifica specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archiviazione**](store.md)
</dt> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
