---
description: Fornisce l'accesso in sola lettura alle proprietà di utilizzo delle chiavi di un certificato.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Oggetto KeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 37b1e33ccb92b2d46effa9f0575f0331fa064e79d172715b8746355d5e99d2b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622271"
---
# <a name="keyusage-object"></a>Oggetto KeyUsage

\[**L'oggetto KeyUsage** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto KeyUsage** fornisce l'accesso in sola lettura alle proprietà di utilizzo delle chiavi di un certificato.

## <a name="members"></a>Membri

**L'oggetto KeyUsage** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto KeyUsage** ha queste proprietà.



| Proprietà                                                                           | Tipo di accesso          | Descrizione                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCritical**](keyusage-iscritical.md)<br/>                               | Sola lettura<br/> | Recupera un valore booleano che indica se **l'estensione KeyUsage** è contrassegnata come critica.<br/>                                  |
| [**IsCRLSignEnabled**](keyusage-iscrlsignenabled.md)<br/>                   | Sola lettura<br/> | Recupera un valore booleano che indica se il bit CRLSign è impostato.<br/>                                                         |
| [**IsDataEnciphermentEnabled**](keyusage-isdataenciphermentenabled.md)<br/> | Sola lettura<br/> | Recupera un valore booleano che indica se il bit dataEncipherment è impostato.<br/>                                                |
| [**IsDecipherOnlyEnabled**](keyusage-isdecipheronlyenabled.md)<br/>         | Sola lettura<br/> | Recupera un valore booleano che indica se il bit decipherOnly è impostato.<br/>                                                    |
| [**IsDigitalSignatureEnabled**](keyusage-isdigitalsignatureenabled.md)<br/> | Sola lettura<br/> | Recupera un valore booleano che indica se il bit digitalSignature è impostato.<br/>                                                |
| [**IsEncipherOnlyEnabled**](keyusage-isencipheronlyenabled.md)<br/>         | Sola lettura<br/> | Recupera un valore booleano che indica se il bit encipherOnly è impostato.<br/>                                                    |
| [**IsKeyAgreementEnabled**](keyusage-iskeyagreementenabled.md)<br/>         | Sola lettura<br/> | Recupera un valore booleano che indica se il bit keyAgreement è impostato.<br/>                                                    |
| [**IsKeyCertSignEnabled**](keyusage-iskeycertsignenabled.md)<br/>           | Sola lettura<br/> | Recupera un valore booleano che indica se il bit keyCertSign è impostato.<br/>                                                     |
| [**IsKeyEnciphermentEnabled**](keyusage-iskeyenciphermentenabled.md)<br/>   | Sola lettura<br/> | Recupera un valore booleano che indica se il bit keyEncipherment è impostato.<br/>                                                 |
| [**IsNonRepudiationEnabled**](keyusage-isnonrepudiationenabled.md)<br/>     | Sola lettura<br/> | Recupera un valore booleano che indica se il bit nonRepudiationEnabled è impostato.<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | Sola lettura<br/> | Recupera un valore booleano che indica se è presente **l'estensione KeyUsage.**<br/> Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile **creare l'oggetto KeyUsage.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> </dl>

 

 
