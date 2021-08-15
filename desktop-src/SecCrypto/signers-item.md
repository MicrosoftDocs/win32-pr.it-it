---
description: Recupera l'oggetto Signer che rappresenta il firmatario indicizzato.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Signers.Item - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33630586282b745da94a442c13a0e85574c5f2e06fc04ab909e4ebf59fc2707b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898408"
---
# <a name="signersitem-property"></a>Signers.Item - proprietà

\[La **proprietà Item** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece una raccolta di oggetti CmsSigner. Per altre informazioni, vedere la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei [**nomi System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà Item** recupera [**l'oggetto Signer**](signer.md) che rappresenta il firmatario indicizzato. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**Signer**](signer.md) che rappresenta il firmatario indicizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firmatari**](signers.md)
</dt> </dl>

 

 
