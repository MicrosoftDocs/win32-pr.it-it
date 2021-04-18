---
description: Determina se le firme sui dati firmati nell'oggetto SignedData sono valide.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: Metodo SignedData. Verify
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
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325147"
---
# <a name="signeddataverify-method"></a>Metodo SignedData. Verify

\[Il metodo **Verify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **Verify** determina se le [*firme*](../secgloss/d-gly.md) sui dati firmati nell'oggetto [**SignedData**](signeddata.md) sono valide. Per verificare una firma, l' [*hash*](../secgloss/h-gly.md) crittografato del contenuto viene decrittografato usando la chiave pubblica del firmatario dal certificato del firmatario. L'hash decrittografato viene confrontato con un nuovo hash del contenuto dei dati. Una firma è valida se gli hash corrispondono. Inoltre, questo metodo compila una catena di certificati per determinare la validità del certificato che fornisce la [*chiave pubblica*](../secgloss/p-gly.md) utilizzata per decrittografare l'hash.

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

*SignedMessage* \[ in\]
</dt> <dd>

Stringa che contiene il messaggio firmato da verificare.

</dd> <dt>

*bDetached* \[ in, facoltativo\]
</dt> <dd>

Se **true**, i dati da firmare sono scollegati. ovvero, il contenuto firmato non è incluso come parte dell'oggetto firmato. Per verificare la firma sul contenuto scollegato, un'applicazione deve disporre di una copia del contenuto originale. Il contenuto scollegato viene spesso utilizzato per ridurre le dimensioni di un oggetto firmato da inviare sul Web, se il destinatario del messaggio firmato dispone di una copia originale dei dati firmati. Il valore predefinito è **False**.

</dd> <dt>

*VerifyFlag* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [ \_ \_ \_ \_ flag di verifica dei dati con firma CAPICOM](capicom-signed-data-verify-flag.md) che indica i criteri di verifica. Il valore predefinito è CAPICOM verificare la \_ \_ firma \_ e il \_ certificato. Utilizzando questo valore, vengono controllati sia la validità del certificato che la validità della firma. Questo parametro può essere impostato per verificare la firma e non il certificato. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                             | Significato                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**CAPICOM \_ verificare solo la \_ firma \_**</dt> </dl>                                   | Viene controllata solo la firma.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**\_verificare la \_ firma e il \_ \_ certificato di CAPICOM**</dt> </dl> | Vengono controllati sia la firma che la validità del certificato utilizzato per creare la firma.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una stringa che contiene i dati firmati codificati.

Se questo metodo ha esito negativo, verrà generato un errore. L'oggetto **Err** conterrà informazioni aggiuntive sull'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
