---
description: Rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: EKU (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331605"
---
# <a name="eku-object"></a>EKU (oggetto)

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L'oggetto **EKU** rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.

## <a name="members"></a>Membri

L'oggetto **EKU** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **EKU** dispone di queste proprietà.



| Proprietà                            | Tipo di accesso           | Descrizione                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome**](eku-name.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera un valore di enumerazione che specifica il nome di CAPICOM dell'EKU. Si tratta della proprietà predefinita.<br/>                                                                                   |
| [**OID**](eku-oid.md)<br/>   | Lettura/Scrittura<br/> | Imposta o Recupera una stringa che contiene un valore stringa OID (EKU [*Object Identifier*](../secgloss/o-gly.md) ) come definito in WinCrypt. h.<br/> |



 

## <a name="remarks"></a>Commenti

L'oggetto **EKU** viene usato dalla raccolta e dalla proprietà seguenti:

-   Raccolta [**EKU**](ekus.md)
-   [**CertificateStatus. EKU**](certificatestatus-eku.md) (proprietà)

Impossibile creare l'oggetto **EKU** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
