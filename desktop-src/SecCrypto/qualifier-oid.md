---
description: Recupera l'ID oggetto del qualificatore.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Qualifier.OID - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42c2f83d4fa8be31991a98b6fe4cfc6a741e2190cd12d54bfd5e968951472bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901051"
---
# <a name="qualifieroid-property"></a>Qualifier.OID - proprietà

\[La **proprietà OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la classe [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri certificato per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione Criteri certificato.\]

La **proprietà OID** recupera l'ID oggetto del qualificatore. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**OID**](oid.md) che identifica il qualificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
