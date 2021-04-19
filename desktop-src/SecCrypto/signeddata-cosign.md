---
description: Crea una firma digitale per il contenuto precedentemente firmato.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: Metodo SignedData. cosign
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
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332824"
---
# <a name="signeddatacosign-method"></a>Metodo SignedData. cosign

\[Il metodo **cosign** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **cosign** crea una [*firma digitale*](../secgloss/d-gly.md) per il contenuto precedentemente firmato.

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

Riferimento all'oggetto [**firmatario**](signer.md) del firmatario dei dati. L'oggetto **firmatario** deve avere accesso alla chiave privata del certificato usato per la firma. Questo parametro può essere **null**. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*EncodingType* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che indica la modalità di codifica dei dati firmati. Il valore predefinito è CAPICOM \_ Encode \_ base64. Questo parametro può avere uno dei valori seguenti.



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
> Quando questo metodo viene chiamato da uno script Web, lo script deve usare la [*chiave privata*](../secgloss/p-gly.md) per creare una firma digitale. Consentire ai siti Web non attendibili di usare la chiave privata costituisce un rischio per la sicurezza. Una finestra di dialogo in cui viene chiesto se il sito Web può utilizzare la chiave privata viene visualizzata quando questo metodo viene chiamato per la prima volta. Se si consente allo script di usare la chiave privata per creare una firma digitale e selezionare "non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per alcuno script all'interno del dominio che usa la chiave privata per creare una firma digitale. Tuttavia, gli script all'esterno del dominio che tentano di usare la chiave privata per creare una firma digitale comporteranno comunque la visualizzazione di questa finestra di dialogo. Se non si consente allo script di utilizzare la chiave privata e selezionare "non visualizzare più questa finestra di dialogo", gli script all'interno di tale dominio verranno automaticamente rifiutati di utilizzare la chiave privata per creare firme digitali.

 

Non è garantito che i cofirmatari siano in un ordine particolare.

I risultati seguenti si applicano al valore del parametro del *firmatario* :

-   Se il parametro del *firmatario* non è **null**, questo metodo usa la chiave privata a cui fa riferimento il certificato associato per crittografare la cofirma. Se la chiave privata a cui fa riferimento il certificato non è disponibile, il metodo ha esito negativo.
-   Se il parametro del *firmatario* è **null** ed è presente esattamente un certificato nell' \_ archivio My dell'utente corrente che ha accesso a una chiave privata, il certificato viene usato per creare la cofirma.
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

 

 
