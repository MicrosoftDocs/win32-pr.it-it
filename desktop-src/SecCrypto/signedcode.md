---
description: Fornisce funzionalità per la firma di file eseguibili con una firma digitale Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Oggetto SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332833"
---
# <a name="signedcode-object"></a>Oggetto SignedCode

\[L'oggetto **SignedCode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

L'oggetto **SignedCode** fornisce la funzionalità per la firma dei file eseguibili con una firma digitale Authenticode.

## <a name="when-to-use"></a>Utilizzo

L'oggetto **SignedCode** viene usato per eseguire le attività seguenti:

-   Firma i file eseguibili.
-   File eseguibili timestamp.
-   Determinare se la firma del file eseguibile è valida.
-   Consente di impostare o recuperare il percorso del file eseguibile.
-   Recuperare il firmatario e l'indicatore di data e ora del file eseguibile.
-   Recuperare una raccolta di certificati per il file eseguibile.
-   Recuperare una descrizione o l'URL per la descrizione del file eseguibile.

## <a name="members"></a>Membri

L'oggetto **SignedCode** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SignedCode** dispone di questi metodi.



| Metodo                                    | Descrizione                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sign**](signedcode-sign.md)           | Crea una firma digitale Authenticode e firma il file eseguibile specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Crea una firma di timestamp Authenticode sul file eseguibile firmato specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .<br/> |
| [**Verificare**](signedcode-verify.md)       | Verifica la firma Authenticode nel file eseguibile firmato specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .<br/>          |



 

### <a name="properties"></a>Proprietà

L'oggetto **SignedCode** dispone di queste proprietà.



| Proprietà                                                       | Tipo di accesso           | Descrizione                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificati**](signedcode-certificates.md)<br/>     | Sola lettura<br/>  | Raccolta di [**certificati**](certificates.md) che contiene tutti i certificati nel file eseguibile firmato.<br/>             |
| [**Descrizione**](signedcode-description.md)<br/>       | Lettura/Scrittura<br/> | Stringa che contiene una descrizione del file eseguibile firmato.<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | Lettura/Scrittura<br/> | Stringa che contiene l'indirizzo HTTP a una descrizione del file eseguibile firmato.<br/>                                         |
| [**FileName**](signedcode-filename.md)<br/>             | Lettura/Scrittura<br/> | Stringa che contiene il percorso del file di contenuto contenente il file eseguibile.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Firmatario**](signedcode-signer.md)<br/>                 | Sola lettura<br/>  | Oggetto [**firmatario**](signer.md) che fornisce l'accesso al firmatario del file eseguibile.<br/>                                    |
| [**Timestamp**](signedcode-timestamper.md)<br/>       | Sola lettura<br/>  | Oggetto [**firmatario**](signer.md) che fornisce l'accesso al timestamp del file eseguibile.<br/>                              |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **SignedCode** e non è sicuro per lo scripting. Il ProgID per l'oggetto **SignedCode** è capicom. SignedCode. 1.

Il file eseguibile deve essere di un tipo che può essere firmato con la tecnologia Authenticode, ad esempio i file con estensione cab, cat, exe, dll, vbs o ocx.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
