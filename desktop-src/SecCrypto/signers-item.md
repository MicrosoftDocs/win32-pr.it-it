---
description: Recupera l'oggetto firmatario che rappresenta il firmatario indicizzato.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Proprietà signers. Item
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
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333559"
---
# <a name="signersitem-property"></a>Proprietà signers. Item

\[La proprietà **Item** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece una raccolta di oggetti CmsSigner. Per ulteriori informazioni, vedere la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Item** recupera l'oggetto [**firmatario**](signer.md) che rappresenta il firmatario indicizzato. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**firmatario**](signer.md) che rappresenta il firmatario indicizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firmatari**](signers.md)
</dt> </dl>

 

 
