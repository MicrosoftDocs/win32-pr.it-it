---
description: Recupera il numero di oggetti certificato nell'insieme.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Proprietà Certificates. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328315"
---
# <a name="certificatescount-property"></a>Proprietà Certificates. Count

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **count** Recupera il numero di oggetti [**certificato**](certificate.md) nella raccolta.

## <a name="syntax"></a>Sintassi


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di oggetti [**certificato**](certificate.md) nella raccolta. Ogni oggetto **certificato** rappresenta un singolo certificato nella raccolta.

## <a name="remarks"></a>Commenti

CAPICOM supporta solo un certificato singolo per l'archivio delle [*Smart Card*](../secgloss/s-gly.md) . Anche se l'archivio delle smart card contiene più di un certificato, questa proprietà conterrà 1. Per ulteriori informazioni sull'archivio delle smart card, vedere il membro dell' **\_ Archivio dell' \_ \_ utente \_ della smart card CAPICOM** dell'enumerazione del [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificati**](certificates.md)
</dt> </dl>

 

 
