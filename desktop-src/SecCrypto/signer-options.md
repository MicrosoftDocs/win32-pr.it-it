---
description: Imposta o recupera l'opzione del certificato del firmatario.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Proprietà Signer. Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330268"
---
# <a name="signeroptions-property"></a>Proprietà Signer. Options

\[La proprietà **options** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **options** imposta o recupera l'opzione del certificato del firmatario.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione di [**\_ \_ \_ Opzioni di inclusione del certificato CAPICOM**](capicom-certificate-include-option.md) che specifica l'opzione del certificato del firmatario. Il valore predefinito è la catena di \_ inclusione del certificato CApicol \_ \_ \_ ad eccezione della \_ radice. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                             | Significato                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**il certificato di \_ CAPICOM \_ include la \_ catena \_ ad eccezione della \_ radice**</dt> </dl> | Salva tutti i certificati nella catena con l'eccezione dell'entità radice.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**il certificato di \_ CAPICOM \_ include l' \_ intera \_ catena**</dt> </dl>                    | Salva la catena di certificati completa.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**il certificato capicol \_ \_ include \_ \_ solo entità finale \_**</dt> </dl>       | Salva solo il certificato dell'entità finale.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firmatario**](signer.md)
</dt> </dl>

 

 
