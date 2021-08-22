---
description: Crea una firma digitale sul contenuto da firmare. Una firma digitale è costituita da un hash del contenuto da firmare crittografato usando la chiave privata del firmatario.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Metodo SignedData.Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6ead7fb1c96b05d6945bb67937b215fd6d5d2422041250bee18e4be26edb2f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899019"
---
# <a name="signeddatasign-method"></a>Metodo SignedData.Sign

\[Il **metodo** Sign è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il **metodo Sign** crea una [*firma*](../secgloss/d-gly.md) digitale sul contenuto da firmare. Una firma digitale è costituita da [*un hash*](../secgloss/h-gly.md) del contenuto da firmare crittografato usando la chiave privata del firmatario. Questo metodo può essere usato solo dopo l'inizializzazione della proprietà [**SignedData.Content.**](signeddata-content.md) Se il **metodo Sign** viene chiamato su un oggetto che ha già una firma, la firma precedente viene sostituita. La firma viene creata usando l'algoritmo di firma SHA1.

## <a name="syntax"></a>Sintassi


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Firmatario* \[ in, facoltativo\]
</dt> <dd>

Riferimento [**all'oggetto Signer**](signer.md) del firmatario dei dati. **L'oggetto Firmatario** deve avere accesso alla [*chiave privata*](../secgloss/p-gly.md) del [*certificato usato*](../secgloss/c-gly.md) per firmare. Questo parametro può essere **NULL.** Per altre informazioni, vedere Osservazioni.

</dd> <dt>

*bDetached* \[ in, facoltativo\]
</dt> <dd>

Se **True,** i dati da firmare vengono scollegati; ciò significa che il contenuto firmato non è incluso nell'oggetto firmato. Per verificare la firma sul contenuto scollegato, un'applicazione deve avere una copia del contenuto originale. Il contenuto scollegato viene spesso usato per ridurre le dimensioni di un oggetto firmato da inviare sul Web, se il destinatario del messaggio firmato ha una copia originale dei dati firmati. Il valore predefinito è **False**.

</dd> <dt>

*EncodingType* \[ in, facoltativo\]
</dt> <dd>

Valore [dell'enumerazione CAPICOM \_ ENCODING \_ TYPE](capicom-encoding-type.md) che indica la modalità di codifica dei dati firmati. Il valore predefinito è CAPICOM \_ ENCODE \_ BASE64. Questo parametro può avere uno dei valori seguenti.



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
> Quando questo metodo viene chiamato da uno script Web, lo script deve usare la chiave privata per creare una firma digitale. Consentire ai siti Web non attendibili di usare la chiave privata è un rischio per la sicurezza. Quando questo metodo viene chiamato per la prima volta, viene visualizzata una finestra di dialogo che chiede se il sito Web può usare la chiave privata. Se si consente allo script di usare la chiave privata per creare una firma digitale e si seleziona "Non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per qualsiasi script all'interno di tale dominio che usa la chiave privata per creare una firma digitale. Tuttavia, gli script esterni a tale dominio che tentano di usare la chiave privata per creare una firma digitale causeranno comunque la visualizzazione di questa finestra di dialogo. Se non si consente allo script di usare la chiave privata e si seleziona "Non visualizzare più questa finestra di dialogo", agli script all'interno di tale dominio verrà automaticamente negata la possibilità di usare la chiave privata per creare firme digitali.

 

Poiché la [](../secgloss/d-gly.md) creazione di una firma digitale richiede l'uso di una chiave [*privata,*](../secgloss/p-gly.md)le applicazioni basate sul Web che tentano di usare questo metodo richiederanno richieste di interfaccia utente che consentono all'utente di approvare l'uso della chiave privata, per motivi di sicurezza.

I risultati seguenti si applicano al *valore del parametro Signer:*

-   Se il *parametro Signer* non è **NULL,** questo metodo usa la chiave privata a cui punta il certificato associato per crittografare la firma. Se la chiave privata a cui punta il certificato non è disponibile, il metodo ha esito negativo.
-   Se il *parametro Signer* è **NULL** ed è presente esattamente un certificato nell'archivio CURRENT USER MY che ha accesso a una chiave privata, tale certificato viene usato per creare \_ la firma.
-   Se il *parametro Signer* è **NULL,** il [**Impostazioni. Il valore della proprietà EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è true ed è presente più di un certificato nell'archivio CURRENT USER MY con una chiave privata disponibile. Verrà visualizzata una finestra di dialogo che consente all'utente di selezionare il certificato \_ usato.
-   Se il *parametro Signer* è **NULL** e l'Impostazioni. [**La proprietà EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è false e il metodo ha esito negativo.
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

 

 
