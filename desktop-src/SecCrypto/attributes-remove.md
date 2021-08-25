---
description: Rimuove un oggetto Attribute indicizzato dalla raccolta.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Metodo Attributes.Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea18aab32153c998a0ddbaced65727e1ecb43dc8c54a7e3989aadcb698693970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879771"
---
# <a name="attributesremove-method"></a>Metodo Attributes.Remove

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il **metodo Remove** rimuove un oggetto [**Attribute**](attribute.md) indicizzato dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Indice [**dell'oggetto Attribute**](attribute.md) da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le applicazioni che usano questo metodo devono contenere codice per gestire un'eccezione generata da questo metodo.

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

 

 
