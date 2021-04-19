---
description: Aggiunge l'oggetto OID specificato alla raccolta.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: OID. Add, metodo
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
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329613"
---
# <a name="oidsadd-method"></a>OID. Add, metodo

\[Il metodo **Add** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **Add** aggiunge l'oggetto [**OID**](oid.md) specificato alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OID* \[ in\]
</dt> <dd>

Oggetto [**OID**](oid.md) da aggiungere alla raccolta. L'oggetto **OID** viene aggiunto nell'ordinamento in base al relativo valore punteggiato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
