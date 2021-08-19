---
description: Crea una firma digitale su contenuto firmato in precedenza.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: Metodo SignedData.CoSign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ed4feb55420ebf9d3bc43496fe3004a4d1b55e1ae8add4e3d5b40ec2ac4ba4ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973891"
---
# <a name="signeddatacosign-method"></a>Metodo SignedData.CoSign

\[Il **metodo CoSign** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il **metodo CoSign** crea una [*firma digitale sul contenuto*](../secgloss/d-gly.md) firmato in precedenza.

## <a name="syntax"></a>Sintassi


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Firmatario* \[ in, facoltativo\]
</dt> <dd>

Riferimento [**all'oggetto Signer**](signer.md) del firmatario dei dati. **L'oggetto Firmatario** deve avere accesso alla chiave privata del certificato usato per firmare. Questo parametro può essere **NULL.** Per altre informazioni, vedere Osservazioni.

</dd> <dt>

*EncodingType* \[ in, facoltativo\]
</dt> <dd>

Valore [**dell'enumerazione CAPICOM \_ ENCODING \_ TYPE**](capicom-encoding-type.md) che indica come devono essere codificati i dati firmati. Il valore predefinito è CAPICOM \_ ENCODE \_ BASE64. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                  | Significato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Questo tipo di codifica viene usato solo quando i dati di input hanno un tipo di codifica sconosciuto. Se questo valore viene usato per specificare il tipo di codifica dell'output, verrà usato CAPICOM \_ ENCODE \_ BASE64. Introduzione a CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPCOM \_ ENCODE \_ BASE64**</dt> </dl> | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**FILE \_ BINARIO DI CODIFICA CAPICOM \_**</dt> </dl> | I dati vengono salvati come sequenza binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una stringa che contiene i dati codificati e firmati.

Se questo metodo ha esito negativo, verrà generato un errore. **L'oggetto Err** conterrà informazioni aggiuntive sull'errore.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve usare la [*chiave privata*](../secgloss/p-gly.md) per creare una firma digitale. Consentire ai siti Web non attendibili di usare la chiave privata è un rischio per la sicurezza. Quando questo metodo viene chiamato per la prima volta, viene visualizzata una finestra di dialogo che chiede se il sito Web può usare la chiave privata. Se si consente allo script di usare la chiave privata per creare una firma digitale e si seleziona "Non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per qualsiasi script all'interno di tale dominio che usa la chiave privata per creare una firma digitale. Tuttavia, gli script esterni a tale dominio che tentano di usare la chiave privata per creare una firma digitale continuano a visualizzare questa finestra di dialogo. Se non si consente allo script di usare la chiave privata e si seleziona "Non visualizzare più questa finestra di dialogo", agli script all'interno di tale dominio verrà automaticamente negata la possibilità di usare la chiave privata per creare firme digitali.

 

Non è garantito che i cofirmatori siano in un ordine specifico.

I risultati seguenti si applicano al *valore del parametro Signer:*

-   Se il *parametro Signer* non è **NULL,** questo metodo usa la chiave privata a cui punta il certificato associato per crittografare l'operazione. Se la chiave privata a cui punta il certificato non è disponibile, il metodo ha esito negativo.
-   Se il *parametro Signer* è **NULL** ed è presente esattamente un certificato nell'archivio CURRENT USER MY che ha accesso a una chiave privata, tale certificato viene usato per creare l'oggetto \_ .
-   Se il *parametro Signer* è **NULL,** il [**Impostazioni. Il valore della proprietà EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è true ed è presente più di un certificato nell'archivio CURRENT USER MY con una chiave privata disponibile. Verrà visualizzata una finestra di dialogo che consente all'utente di selezionare il certificato \_ usato.
-   Se il *parametro Signer* è **NULL** e l'Impostazioni. [**La proprietà EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è false. Il metodo ha esito negativo.
-   Se il *parametro Signer* è **NULL** e non è presente alcun certificato nell'archivio CURRENT USER MY con una chiave \_ privata disponibile, il metodo ha esito negativo.

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

 

 
