---
description: Recupera i dati con hash dopo le chiamate al metodo hash.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: Proprietà HashedData. Value
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
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325598"
---
# <a name="hasheddatavalue-property"></a>Proprietà HashedData. Value

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **value** recupera i dati con hash dopo le chiamate al metodo [**hash**](hasheddata-hash.md) . Il valore hash viene restituito in formato esadecimale. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Valore proprietà

Stringa che contiene i dati con hash in formato esadecimale.

## <a name="remarks"></a>Commenti

Per creare l'hash di una grande quantità di dati, chiamare il metodo [**hash**](hasheddata-hash.md) per ogni pezzo di dati. L'hash di ogni porzione di dati viene concatenato alla proprietà **value** fino a quando non viene letta la proprietà. Il contenuto della proprietà **value** viene reimpostato quando viene letta la proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
