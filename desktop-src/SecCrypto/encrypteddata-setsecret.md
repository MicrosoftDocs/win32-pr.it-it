---
description: Imposta il valore del segreto utilizzato per derivare la chiave di sessione crittografica utilizzata per crittografare e decrittografare i dati.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Metodo EncryptedData.SetSecret
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
ms.openlocfilehash: 0e56bd490c4e665d900eb39fb57d09019ab4cfa3b1eb3ad06ad74cb4e83514ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766446"
---
# <a name="encrypteddatasetsecret-method"></a>Metodo EncryptedData.SetSecret

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni api Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi. Per informazioni su PInvoke, vedere [Esercitazione su Platform Invoke.](https://msdn.microsoft.com/library/aa288468.aspx) Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

Il **metodo SetSecret** imposta il valore del segreto usato per derivare la chiave di sessione crittografica [*usata*](../secgloss/s-gly.md) per crittografare e decrittografare i dati.

## <a name="syntax"></a>Sintassi


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Stringa contenente un segreto utilizzato per creare una chiave crittografica di sessione.

</dd> <dt>

*SecretType* \[ in, facoltativo\]
</dt> <dd>

Valore [**dell'enumerazione CAPICOM \_ SECRET \_ TYPE**](capicom-secret-type.md) che indica il tipo di segreto usato per generare la chiave di sessione. Il valore predefinito è CAPICOM \_ SECRET \_ PASSWORD. Questo parametro può essere il valore seguente.



| Valore                                                                                                                                                                                        | Significato                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**PASSWORD SEGRETA CAPICOM \_ \_**</dt> </dl> | La chiave di crittografia deve essere derivata da una password.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il segreto viene usato per creare la chiave di sessione per la crittografia o la decrittografia. Lo stesso segreto deve essere usato per entrambe le operazioni. Se il segreto usato per crittografare i dati viene perso, i dati crittografati non possono essere decrittografati.

Se appropriato per l'applicazione, è consigliabile usare [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) o [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) per proteggere il segreto prima e dopo l'uso. Al termine, cancellare la memoria associata al segreto.

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

[**Encrypteddata**](encrypteddata.md)
</dt> </dl>

 

 
