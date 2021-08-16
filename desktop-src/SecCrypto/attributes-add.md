---
description: Aggiunge un oggetto Attribute alla raccolta.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Metodo Attributes.Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5639a4bed96dcf4cef315b4550cd2982778d6ecc68024364f06eb377cbd8b0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773516"
---
# <a name="attributesadd-method"></a>Metodo Attributes.Add

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la classe [**CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/previous-versions/windows/)\]

Il **metodo Add** aggiunge un oggetto [**Attribute**](attribute.md) alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Attributo* \[ Pollici\]
</dt> <dd>

Oggetto [**Attribute**](attribute.md) da aggiungere alla fine dell'insieme.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Un'applicazione che usa questo metodo deve contenere codice per gestire un'eccezione generata da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti di crittografia](cryptography-objects.md)
</dt> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 
