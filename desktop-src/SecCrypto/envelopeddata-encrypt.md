---
description: Genera una chiave di sessione e crittografa i dati e le buste.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: Metodo EnvelopedData. Encrypt
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
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327093"
---
# <a name="envelopeddataencrypt-method"></a>Metodo EnvelopedData. Encrypt

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **Encrypt** genera una chiave di sessione, USA tale chiave per crittografare il contenuto, racchiude il contenuto crittografato per ogni destinatario crittografando la chiave della sessione con la chiave pubblica di ogni destinatario, quindi restituisce il [*BLOB*](../secgloss/b-gly.md) che contiene il contenuto crittografato e le chiavi della sessione crittografata come stringa codificata.

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

Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che indica il tipo di codifica utilizzato per codificare i dati in busta digitale. Il valore di codifica predefinito è CAPICOM \_ Encode \_ base64. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                  | Significato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Encode \_ any**</dt> </dl>          | Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto. Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64. Introdotta in capicol 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Codifica Base64 per CAPICOM \_**</dt> </dl> | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_codificare il \_ file binario di CAPICOM**</dt> </dl> | I dati vengono salvati come una sequenza binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un BLOB che contiene i dati in busta in una stringa codificata.

## <a name="remarks"></a>Commenti

Il BLOB restituito contiene il contenuto crittografato e una chiave di sessione crittografata per ogni destinatario previsto. Queste chiavi di sessione vengono crittografate con la chiave pubblica di ogni destinatario. Le chiavi della sessione crittografata possono essere decrittografate solo con la chiave privata di un destinatario.

Se la proprietà [**Recipients**](envelopeddata-recipients.md) non contiene informazioni, questo metodo cerca i destinatari potenziali nell'archivio certificati AddressBook dell'utente corrente. Se viene trovato più di un potenziale destinatario, all'utente viene richiesto di selezionare un destinatario da una finestra di dialogo di selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
