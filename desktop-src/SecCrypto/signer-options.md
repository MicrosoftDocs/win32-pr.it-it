---
description: Imposta o recupera l'opzione del certificato del firmatario.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Proprietà Signer.Options
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
ms.openlocfilehash: 7b4a787524e967b5356ed7fb5531a3ec7d7dbfb99d57fc75217a82f220468db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898837"
---
# <a name="signeroptions-property"></a>Proprietà Signer.Options

\[La **proprietà** Opzioni è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà Options** imposta o recupera l'opzione del certificato del firmatario.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Valore proprietà

Valore [**dell'enumerazione CAPICOM \_ CERTIFICATE INCLUDE \_ \_ OPTION**](capicom-certificate-include-option.md) che specifica l'opzione del certificato del firmatario. Il valore predefinito è CAPICOM \_ CERTIFICATE INCLUDE CHAIN EXCEPT \_ \_ \_ \_ ROOT. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                             | Significato                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CATENA DI INCLUSIONE DEL CERTIFICATO CAPICOM \_ \_ AD ECCEZIONE DELLA \_ \_ \_ RADICE**</dt> </dl> | Salva tutti i certificati nella catena, ad eccezione dell'entità radice.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**IL CERTIFICATO CAPICOM \_ \_ INCLUDE \_ L'INTERA \_ CATENA**</dt> </dl>                    | Salva la catena di certificati completa.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**IL CERTIFICATO CAPICOM \_ \_ INCLUDE SOLO ENTITÀ \_ \_ \_ FINALE**</dt> </dl>       | Salva solo il certificato dell'entità finale.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firmatario**](signer.md)
</dt> </dl>

 

 
