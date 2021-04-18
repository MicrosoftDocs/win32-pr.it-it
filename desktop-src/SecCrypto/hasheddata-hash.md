---
description: Crea un hash della stringa specificata.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Metodo HashedData. hash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325599"
---
# <a name="hasheddatahash-method"></a>Metodo HashedData. hash

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **hash** crea un hash della stringa specificata.

## <a name="syntax"></a>Sintassi


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

Stringa che contiene il valore di cui eseguire l'hashing.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per creare l'hash di una grande quantità di dati, chiamare il metodo **hash** per ogni pezzo di dati. L'hash di ogni porzione di dati viene concatenato alla proprietà [**value**](hasheddata-value.md) fino a quando non viene letta la proprietà. Il contenuto della proprietà **value** viene reimpostato quando viene letta la proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
