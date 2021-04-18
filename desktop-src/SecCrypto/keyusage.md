---
description: Fornisce accesso in sola lettura alle proprietà di utilizzo delle chiavi di un certificato.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: DataUsage (oggetto)
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
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323944"
---
# <a name="keyusage-object"></a>DataUsage (oggetto)

\[L'oggetto **DataUsage** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **DataUsage** fornisce accesso in sola lettura alle proprietà di utilizzo delle chiavi di un certificato.

## <a name="members"></a>Membri

L'oggetto **DataUsage** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **DataUsage** dispone di queste proprietà.



| Proprietà                                                                           | Tipo di accesso          | Descrizione                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCritical**](keyusage-iscritical.md)<br/>                               | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione per l' **utilizzo dei dati** è contrassegnata come critica.<br/>                                  |
| [**IsCRLSignEnabled**](keyusage-iscrlsignenabled.md)<br/>                   | Sola lettura<br/> | Recupera un valore booleano che indica se il bit bit crlsign è impostato.<br/>                                                         |
| [**IsDataEnciphermentEnabled**](keyusage-isdataenciphermentenabled.md)<br/> | Sola lettura<br/> | Recupera un valore booleano che indica se il bit dataEncipherment è impostato.<br/>                                                |
| [**IsDecipherOnlyEnabled**](keyusage-isdecipheronlyenabled.md)<br/>         | Sola lettura<br/> | Recupera un valore booleano che indica se il bit decipherOnly è impostato.<br/>                                                    |
| [**IsDigitalSignatureEnabled**](keyusage-isdigitalsignatureenabled.md)<br/> | Sola lettura<br/> | Recupera un valore booleano che indica se il bit digitalSignature è impostato.<br/>                                                |
| [**IsEncipherOnlyEnabled**](keyusage-isencipheronlyenabled.md)<br/>         | Sola lettura<br/> | Recupera un valore booleano che indica se il bit encipherOnly è impostato.<br/>                                                    |
| [**IsKeyAgreementEnabled**](keyusage-iskeyagreementenabled.md)<br/>         | Sola lettura<br/> | Recupera un valore booleano che indica se è stato impostato il bit di un contratto.<br/>                                                    |
| [**IsKeyCertSignEnabled**](keyusage-iskeycertsignenabled.md)<br/>           | Sola lettura<br/> | Recupera un valore booleano che indica se il bit bit keycertsign è impostato.<br/>                                                     |
| [**IsKeyEnciphermentEnabled**](keyusage-iskeyenciphermentenabled.md)<br/>   | Sola lettura<br/> | Recupera un valore booleano che indica se il bit keyEncipherment è impostato.<br/>                                                 |
| [**IsNonRepudiationEnabled**](keyusage-isnonrepudiationenabled.md)<br/>     | Sola lettura<br/> | Recupera un valore booleano che indica se il bit nonRepudiationEnabled è impostato.<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | Sola lettura<br/> | Recupera un valore booleano che indica se l'estensione per l' **utilizzo di dati** è presente.<br/> Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile creare l'oggetto **DataUsage** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> </dl>

 

 
