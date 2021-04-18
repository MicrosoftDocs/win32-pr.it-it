---
description: Crea una firma digitale sul contenuto da firmare. Una firma digitale è costituita da un hash del contenuto da firmare crittografato tramite la chiave privata del firmatario.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Metodo SignedData. Sign
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
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325150"
---
# <a name="signeddatasign-method"></a>Metodo SignedData. Sign

\[Il metodo **Sign** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **Sign** crea una [*firma digitale*](../secgloss/d-gly.md) sul contenuto da firmare. Una firma digitale è costituita da un [*hash*](../secgloss/h-gly.md) del contenuto da firmare crittografato tramite la chiave privata del firmatario. Questo metodo può essere utilizzato solo dopo l'inizializzazione della proprietà [**SignedData. Content**](signeddata-content.md) . Se il metodo **Sign** viene chiamato su un oggetto che dispone già di una firma, la firma precedente viene sostituita. La firma viene creata utilizzando l'algoritmo di firma SHA1.

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

Riferimento all'oggetto [**firmatario**](signer.md) del firmatario dei dati. L'oggetto **firmatario** deve avere accesso alla [*chiave privata*](../secgloss/p-gly.md) del [*certificato*](../secgloss/c-gly.md) usato per la firma. Questo parametro può essere **null**. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*bDetached* \[ in, facoltativo\]
</dt> <dd>

Se **true**, i dati da firmare sono scollegati. ovvero, il contenuto firmato non è incluso come parte dell'oggetto firmato. Per verificare la firma sul contenuto scollegato, un'applicazione deve disporre di una copia del contenuto originale. Il contenuto scollegato viene spesso utilizzato per ridurre le dimensioni di un oggetto firmato da inviare sul Web, se il destinatario del messaggio firmato dispone di una copia originale dei dati firmati. Il valore predefinito è **False**.

</dd> <dt>

*EncodingType* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [ \_ \_ tipo di codifica CAPICOM](capicom-encoding-type.md) che indica la modalità di codifica dei dati firmati. Il valore predefinito è CAPICOM \_ Encode \_ base64. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                  | Significato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Encode \_ any**</dt> </dl>          | Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto. Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64. Introdotta in capicol 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Codifica Base64 per CAPICOM \_**</dt> </dl> | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_codificare il \_ file binario di CAPICOM**</dt> </dl> | I dati vengono salvati come una sequenza binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una stringa che contiene i dati firmati codificati.

Se questo metodo ha esito negativo, verrà generato un errore. L'oggetto **Err** conterrà informazioni aggiuntive sull'errore.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve usare la chiave privata per creare una firma digitale. Consentire ai siti Web non attendibili di usare la chiave privata costituisce un rischio per la sicurezza. Una finestra di dialogo in cui viene chiesto se il sito Web può utilizzare la chiave privata viene visualizzata quando questo metodo viene chiamato per la prima volta. Se si consente allo script di usare la chiave privata per creare una firma digitale e selezionare "non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per alcuno script all'interno del dominio che usa la chiave privata per creare una firma digitale. Tuttavia, gli script all'esterno del dominio che tentano di usare la chiave privata per creare una firma digitale comporteranno comunque la visualizzazione di questa finestra di dialogo. Se non si consente allo script di utilizzare la chiave privata e selezionare "non visualizzare più questa finestra di dialogo", gli script all'interno di tale dominio verranno automaticamente rifiutati di utilizzare la chiave privata per creare firme digitali.

 

Poiché la creazione di una [*firma digitale*](../secgloss/d-gly.md) richiede l'uso di una [*chiave privata*](../secgloss/p-gly.md), le applicazioni basate sul Web che tentano di usare questo metodo richiederanno richieste di interfaccia utente che consentono all'utente di approvare l'uso della chiave privata, per motivi di sicurezza.

I risultati seguenti si applicano al valore del parametro del *firmatario* :

-   Se il parametro del *firmatario* non è **null**, questo metodo usa la chiave privata a cui fa riferimento il certificato associato per crittografare la firma. Se la chiave privata a cui fa riferimento il certificato non è disponibile, il metodo ha esito negativo.
-   Se il parametro del *firmatario* è **null** ed è presente esattamente un certificato nell' \_ archivio My dell'utente corrente che ha accesso a una chiave privata, il certificato viene usato per creare la firma.
-   Se il parametro del *firmatario* è **null**, il valore della proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è true ed esiste più di un certificato nell' \_ archivio My dell'utente corrente con una chiave privata disponibile, viene visualizzata una finestra di dialogo che consente all'utente di selezionare il certificato usato.
-   Se il parametro del *firmatario* è **null** e la proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è false, il metodo ha esito negativo.
-   Se il parametro del *firmatario* è **null** e non è presente alcun certificato nell' \_ utente corrente My Store con una chiave privata disponibile, il metodo ha esito negativo.

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

 

 
