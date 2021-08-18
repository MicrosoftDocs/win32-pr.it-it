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
ms.openlocfilehash: e119a639af7cb6459e8e6ec8ae6416f9d067c56e8f81560fedc385abd518b840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899340"
---
# <a name="signedcode-object"></a>Oggetto SignedCode

\[**L'oggetto SignedCode** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

**L'oggetto SignedCode** fornisce funzionalità per la firma di file eseguibili con una firma digitale Authenticode.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto SignedCode** viene usato per eseguire le attività seguenti:

-   Firmare i file eseguibili.
-   File eseguibili del timestamp.
-   Determinare se la firma del file eseguibile è valida.
-   Impostare o recuperare il percorso del file eseguibile.
-   Recuperare il firmatario e il timestamp del file eseguibile.
-   Recuperare una raccolta di certificati per il file eseguibile.
-   Recuperare una descrizione o l'URL della descrizione del file eseguibile.

## <a name="members"></a>Membri

**L'oggetto SignedCode** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SignedCode** dispone di questi metodi.



| Metodo                                    | Descrizione                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Segno**](signedcode-sign.md)           | Crea una firma digitale Authenticode e firma il file eseguibile specificato nella [**proprietà SignedCode.FileName.**](signedcode-filename.md)<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Crea una firma timestamp Authenticode nel file eseguibile firmato specificato nella [**proprietà SignedCode.FileName.**](signedcode-filename.md)<br/> |
| [**Verificare**](signedcode-verify.md)       | Verifica la firma Authenticode nel file eseguibile firmato specificato nella [**proprietà SignedCode.FileName.**](signedcode-filename.md)<br/>          |



 

### <a name="properties"></a>Proprietà

**L'oggetto SignedCode** ha queste proprietà.



| Proprietà                                                       | Tipo di accesso           | Descrizione                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificati**](signedcode-certificates.md)<br/>     | Sola lettura<br/>  | Raccolta [**Certificates**](certificates.md) che contiene tutti i certificati nel file eseguibile firmato.<br/>             |
| [**Descrizione**](signedcode-description.md)<br/>       | Lettura/Scrittura<br/> | Stringa che contiene una descrizione del file eseguibile firmato.<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | Lettura/Scrittura<br/> | Stringa contenente l'indirizzo HTTP di una descrizione del file eseguibile firmato.<br/>                                         |
| [**Filename**](signedcode-filename.md)<br/>             | Lettura/Scrittura<br/> | Stringa che contiene il percorso del file di contenuto che contiene il file eseguibile.<br/> Si tratta della proprietà predefinita.<br/> |
| [**Firmatario**](signedcode-signer.md)<br/>                 | Sola lettura<br/>  | Oggetto [**Signer**](signer.md) che fornisce l'accesso al firmatario del file eseguibile.<br/>                                    |
| [**Timestamper**](signedcode-timestamper.md)<br/>       | Sola lettura<br/>  | Oggetto [**Signer**](signer.md) che fornisce l'accesso al timestamp del file eseguibile.<br/>                              |



 

## <a name="remarks"></a>Commenti

**L'oggetto SignedCode** può essere creato e non è sicuro per lo scripting. Il ProgID per **l'oggetto SignedCode** è CAPICOM. SignedCode.1.

Il file eseguibile deve essere di un tipo che può essere firmato con la tecnologia Authenticode, ad esempio file con estensione .cab, cat, .exe, .dll, vbs o ocx.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
