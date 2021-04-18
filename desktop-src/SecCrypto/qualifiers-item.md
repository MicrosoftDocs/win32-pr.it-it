---
description: Recupera un qualificatore in base a un indice specificato.
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: Proprietà Qualifiers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331270"
---
# <a name="qualifiersitem-property"></a>Proprietà Qualifiers. Item

\[La proprietà **Item** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]

La proprietà **Item** recupera un qualificatore in base a un indice specificato. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**qualificatore**](qualifier.md) che rappresenta il qualificatore indicizzato della raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori**](qualifiers.md)
</dt> </dl>

 

 
