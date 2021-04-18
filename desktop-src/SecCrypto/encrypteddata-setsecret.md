---
description: Imposta il valore del segreto utilizzato per derivare la chiave della sessione crittografica utilizzata per crittografare e decrittografare i dati.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData. sesecret, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324897"
---
# <a name="encrypteddatasetsecret-method"></a>EncryptedData. sesecret, metodo

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

Il metodo **sesecret** imposta il valore del segreto usato per derivare la chiave della [*sessione*](../secgloss/s-gly.md) crittografica usata per crittografare e decrittografare i dati.

## <a name="syntax"></a>Sintassi


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Stringa che contiene un segreto utilizzato per creare una chiave crittografica della sessione.

</dd> <dt>

*SecretType* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ tipo di segreto CAPICOM**](capicom-secret-type.md) che indica il tipo di segreto usato per generare la chiave della sessione. Il valore predefinito è CAPICOM \_ Secret \_ password. Questo parametro può essere il valore seguente.



| Valore                                                                                                                                                                                        | Significato                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**PASSWORD del segreto di CAPICOM \_ \_**</dt> </dl> | La chiave di crittografia deve essere derivata da una password.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il segreto viene usato per creare la chiave di sessione per la crittografia o la decrittografia. Per entrambe le operazioni è necessario usare lo stesso segreto. Se il segreto utilizzato per crittografare i dati viene perso, non sarà possibile decrittografare i dati crittografati.

Se appropriato per l'applicazione, prendere in considerazione l'uso di [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) o [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) per proteggere il segreto prima e dopo l'uso. Al termine, cancellare la memoria associata al segreto.

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

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
