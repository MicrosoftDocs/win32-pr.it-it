---
description: Imposta o recupera la chiave privata associata al certificato.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Certificate.PrivateKey - proprietà
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
ms.openlocfilehash: 18e6acc2aa4b765e9219eff479280df814f1089dc27366c5d175dcdeda4fd890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771556"
---
# <a name="certificateprivatekey-property"></a>Certificate.PrivateKey - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà PrivateKey** imposta o recupera la chiave privata associata al certificato. Questa proprietà è stata introdotta in CAPICOM 2.0.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**PrivateKey**](privatekey.md) che rappresenta la chiave privata associata al certificato.

## <a name="remarks"></a>Commenti

**L'impostazione della proprietà PrivateKey** su Nothing rimuove l'associazione tra la chiave privata e il certificato, ma non elimina la chiave privata. Per eliminare la chiave privata, chiamare il [**metodo PrivateKey.Delete**](privatekey-delete.md) e quindi impostare questa proprietà su Nothing.

Questa proprietà genera CAPICOM \_ E NOT ALLOWED quando viene \_ \_ impostata da un'applicazione basata sul Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
