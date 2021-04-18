---
description: Imposta o recupera l'oggetto certificato che rappresenta il certificato di un firmatario dei dati.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Proprietà Signer. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324461"
---
# <a name="signercertificate-property"></a>Proprietà Signer. Certificate

\[La proprietà **certificato** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Certificate** imposta o recupera l'oggetto [**certificato**](certificate.md) che rappresenta il certificato di un firmatario dei dati. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**certificato**](certificate.md) che rappresenta il certificato di un firmatario dei dati.

## <a name="remarks"></a>Commenti

Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firmatario**](signer.md)
</dt> </dl>

 

 
