---
description: Aggiunge un oggetto attributo alla raccolta.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Metodo Attributes. Add
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
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332692"
---
# <a name="attributesadd-method"></a>Metodo Attributes. Add

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]

Il metodo **Add** aggiunge un oggetto [**attribute**](attribute.md) alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Attributo* \[ in\]
</dt> <dd>

Oggetto [**attributo**](attribute.md) da aggiungere alla fine della raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Un'applicazione che usa questo metodo deve contenere codice per gestire un'eccezione generata da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Cryptography](cryptography-objects.md)
</dt> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 
