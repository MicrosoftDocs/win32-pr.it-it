---
description: Recupera i dati con hash dopo le chiamate riuscite al metodo Hash.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData.Value - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a6b8b2c8291e793cd88c5d4b0821c036fb6b112beb87e73d4f8ccb8d523deb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006569"
---
# <a name="hasheddatavalue-property"></a>HashedData.Value - proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà Value** recupera i dati con hash dopo le chiamate riuscite al metodo [**Hash.**](hasheddata-hash.md) Il valore hash viene restituito in formato esadecimale. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Valore proprietà

Stringa contenente i dati con hash in formato esadecimale.

## <a name="remarks"></a>Commenti

Per creare l'hash di una grande quantità di dati, chiamare il [**metodo Hash**](hasheddata-hash.md) per ogni dato. L'hash di ogni dato viene concatenato alla **proprietà Value** finché la proprietà non viene letta. Il contenuto della **proprietà Value** viene reimpostato quando la proprietà viene letta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
