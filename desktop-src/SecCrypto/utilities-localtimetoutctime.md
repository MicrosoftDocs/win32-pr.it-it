---
description: Converte l'ora locale del computer in Coordinated Universal Time (ora di Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Metodo Utilities.LocalTimeToUTCTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 03efb6cdfbea712f2fbca194073b89bcee66975481c1a7c0fdc2d7bd385eb652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971022"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Metodo Utilities.LocalTimeToUTCTime

\[Il **metodo LocalTimeToUTCTime** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.\]

Il **metodo LocalTimeToUTCTime** converte l'ora locale del computer Coordinated Universal Time (ora di Greenwich).

## <a name="syntax"></a>Sintassi


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LocalTime* \[ Pollici\]
</dt> <dd>

Ora locale da convertire in Coordinated Universal Time.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore Coordinated Universal Time corrispondente all'ora locale specificata.

## <a name="remarks"></a>Commenti

Mentre il sistema usa Coordinated Universal Time internamente, le applicazioni visualizzano in genere l'ora locale, ovvero la data e l'ora del giorno per il fuso orario locale del computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Utilità**](utilities.md)
</dt> </dl>

 

 




