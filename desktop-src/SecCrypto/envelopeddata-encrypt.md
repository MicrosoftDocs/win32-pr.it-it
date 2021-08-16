---
description: Genera una chiave di sessione e crittografa e inviluppo i dati.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: Metodo EnvelopedData.Encrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df4741538ae11dbe1b158fd9b8e8a6c8632c427f9a0e8376e8cd10c9056461fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766088"
---
# <a name="envelopeddataencrypt-method"></a>Metodo EnvelopedData.Encrypt

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il metodo **Encrypt** genera una chiave di sessione, usa tale chiave per crittografare il contenuto, avvolgono il contenuto crittografato per ogni destinatario crittografando la chiave di sessione con la chiave pubblica di ogni destinatario e quindi restituisce il [*BLOB*](../secgloss/b-gly.md) che contiene il contenuto crittografato e le chiavi di sessione crittografate come stringa codificata.

## <a name="syntax"></a>Sintassi


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncodingType* \[ in, facoltativo\]
</dt> <dd>

Valore [**dell'enumerazione CAPICOM \_ ENCODING \_ TYPE**](capicom-encoding-type.md) che indica il tipo di codifica utilizzato per codificare i dati in busta. Il valore di codifica predefinito è CAPICOM \_ ENCODE \_ BASE64. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                  | Significato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Questo tipo di codifica viene usato solo quando i dati di input hanno un tipo di codifica sconosciuto. Se questo valore viene usato per specificare il tipo di codifica dell'output, verrà usato CAPICOM \_ ENCODE \_ BASE64. Introduzione a CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPCOM \_ ENCODE \_ BASE64**</dt> </dl> | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**FILE \_ BINARIO DI CODIFICA CAPICOM \_**</dt> </dl> | I dati vengono salvati come sequenza binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un BLOB che contiene i dati in busta in una stringa codificata.

## <a name="remarks"></a>Commenti

Il BLOB restituito contiene il contenuto crittografato e una chiave di sessione crittografata per ogni destinatario previsto. Queste chiavi di sessione vengono crittografate usando la chiave pubblica di ogni destinatario. Le chiavi di sessione crittografate possono essere decrittografate solo con la chiave privata di un destinatario.

Se la [**proprietà Recipients**](envelopeddata-recipients.md) non contiene informazioni, questo metodo cerca i potenziali destinatari nell'archivio certificati AddressBook dell'utente corrente. Se viene trovato più di un potenziale destinatario, all'utente viene richiesto di selezionare un destinatario da una finestra di dialogo di selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
