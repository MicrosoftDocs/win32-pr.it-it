---
description: Aggiunge l'oggetto OID specificato alla raccolta.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Metodo OIDs.Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff686ae816fa61d68e0a0c40326581025ced8f4c94fb5cffc633ff452ac4f0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979652"
---
# <a name="oidsadd-method"></a>Metodo OIDs.Add

\[Il **metodo** Add è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe OidCollection nello**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il **metodo Add** aggiunge l'oggetto [**OID**](oid.md) specificato alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OID* \[ Pollici\]
</dt> <dd>

Oggetto [**OID**](oid.md) da aggiungere alla raccolta. **L'oggetto OID** viene aggiunto nell'ordinamento in base al relativo valore punteggiato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
