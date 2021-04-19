---
description: Recupera un oggetto dalla raccolta di destinatari.
ms.assetid: 03600d4a-5fd4-45c7-ae91-efdc26c084ee
title: Proprietà Recipients. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a80b472c8257597356c626a9e88aad97c447f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326351"
---
# <a name="recipientsitem-property"></a>Proprietà Recipients. Item

\[La proprietà **Item** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Item** recupera un oggetto dalla raccolta [**Recipients**](recipients.md) . Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
Recipients.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valore proprietà

Variant che rappresenta l'elemento indicizzato nella raccolta di [**destinatari**](recipients.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Destinatari**](recipients.md)
</dt> </dl>

 

 
