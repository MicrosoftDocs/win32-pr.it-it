---
description: Rappresenta una singola proprietà EKU (Extended Key Usage) di un certificato.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Oggetto EKU
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
ms.openlocfilehash: bd887204abc31583e596e94c25b64addcfe8109e6432845d25d939fd8e79e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875141"
---
# <a name="eku-object"></a>Oggetto EKU

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto EKU** rappresenta una singola proprietà EKU (Extended Key Usage) di un certificato.

## <a name="members"></a>Membri

**L'oggetto EKU** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto EKU** ha queste proprietà.



| Proprietà                            | Tipo di accesso           | Descrizione                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nome**](eku-name.md)<br/> | Lettura/Scrittura<br/> | Imposta o recupera un valore di enumerazione che specifica il nome CAPICOM dell'EKU. Si tratta della proprietà predefinita.<br/>                                                                                   |
| [**Oid**](eku-oid.md)<br/>   | Lettura/Scrittura<br/> | Imposta o recupera una stringa che contiene un valore stringa OID (EKU [*Object Identifier)*](../secgloss/o-gly.md) come definito in Wincrypt.h.<br/> |



 

## <a name="remarks"></a>Commenti

**L'oggetto EKU** viene usato dalla raccolta e dalla proprietà seguenti:

-   [**Raccolta di EKU**](ekus.md)
-   [**Proprietà CertificateStatus.EKU**](certificatestatus-eku.md)

Non è possibile creare l'oggetto **EKU.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
