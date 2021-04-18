---
description: Imposta o recupera la chiave privata associata al certificato.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Proprietà Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333959"
---
# <a name="certificateprivatekey-property"></a>Proprietà Certificate. PrivateKey

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **PrivateKey** imposta o recupera la chiave privata associata al certificato. Questa proprietà è stata introdotta in capicol 2,0.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**PrivateKey**](privatekey.md) che rappresenta la chiave privata associata al certificato.

## <a name="remarks"></a>Commenti

Se si imposta la proprietà **PrivateKey** su Nothing, viene rimossa l'associazione tra la chiave privata e il certificato, ma la chiave privata non viene eliminata. Per eliminare la chiave privata, chiamare il metodo [**PrivateKey. Delete**](privatekey-delete.md) , quindi impostare questa proprietà su Nothing.

Questa proprietà genera CAPICOM \_ E \_ non \_ è consentita quando viene impostata da un'applicazione basata sul Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
