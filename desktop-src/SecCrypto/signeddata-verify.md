---
description: Determina se le firme sui dati firmati nell'oggetto SignedData sono valide.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: Metodo SignedData.Verify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ccda81fc3640d4d09f9644bdf0d84a18a68b743397e1578a5ad434349893e893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898975"
---
# <a name="signeddataverify-method"></a>Metodo SignedData.Verify

\[Il **metodo** Verify è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il **metodo Verify** determina se le firme [*sui*](../secgloss/d-gly.md) dati firmati nell'oggetto [**SignedData**](signeddata.md) sono valide. Per verificare una firma, [*l'hash*](../secgloss/h-gly.md) crittografato del contenuto viene decrittografato usando la chiave pubblica del firmatario dal certificato del firmatario. L'hash decrittografato viene confrontato con un nuovo hash del contenuto dei dati. Una firma è valida se gli hash corrispondono. Inoltre, questo metodo compila anche una catena di certificati per determinare la validità del certificato che fornisce la [*chiave pubblica*](../secgloss/p-gly.md) usata per decrittografare l'hash.

## <a name="syntax"></a>Sintassi


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SignedMessage* \[ Pollici\]
</dt> <dd>

Stringa contenente il messaggio firmato da verificare.

</dd> <dt>

*bDetached* \[ in, facoltativo\]
</dt> <dd>

Se **True,** i dati da firmare vengono scollegati; ciò significa che il contenuto firmato non è incluso nell'oggetto firmato. Per verificare la firma sul contenuto scollegato, un'applicazione deve avere una copia del contenuto originale. Il contenuto scollegato viene spesso usato per ridurre le dimensioni di un oggetto firmato da inviare sul Web, se il destinatario del messaggio firmato ha una copia originale dei dati firmati. Il valore predefinito è **False**.

</dd> <dt>

*VerifyFlag* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione [CAPICOM \_ SIGNED DATA VERIFY \_ \_ \_ FLAG](capicom-signed-data-verify-flag.md) che indica i criteri di verifica. Il valore predefinito è CAPICOM \_ VERIFY \_ SIGNATURE AND \_ \_ CERTIFICATE. Usando questo valore, vengono verificate sia la validità del certificato che la validità della firma. Questo parametro può essere impostato per verificare la firma e non il certificato. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                             | Significato                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**SOLO FIRMA DI VERIFICA \_ \_ \_ CAPICOM**</dt> </dl>                                   | Viene verificata solo la firma.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**VERIFICA DELLA FIRMA \_ \_ E DEL \_ \_ CERTIFICATO DI CAPICOM**</dt> </dl> | Vengono controllati sia la firma che la validità del certificato usato per creare la firma.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una stringa che contiene i dati codificati e firmati.

Se questo metodo ha esito negativo, verrà generato un errore. **L'oggetto Err** conterrà informazioni aggiuntive sull'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
