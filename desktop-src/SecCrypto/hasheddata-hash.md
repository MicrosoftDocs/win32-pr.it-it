---
description: Crea un hash della stringa specificata.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Metodo HashedData.Hash
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
ms.openlocfilehash: 2828f54f754591d1b0027a6c892dc57e8b5cdfecc5e9759985b74b1dffef9fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006579"
---
# <a name="hasheddatahash-method"></a>Metodo HashedData.Hash

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il **metodo Hash** crea un hash della stringa specificata.

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

Stringa contenente il valore di cui eseguire l'hashing.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per creare l'hash di una grande quantità di dati, chiamare il **metodo Hash** per ogni dato. L'hash di ogni dato viene concatenato alla [**proprietà Value**](hasheddata-value.md) finché la proprietà non viene letta. Il contenuto della **proprietà Value** viene reimpostato quando la proprietà viene letta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
