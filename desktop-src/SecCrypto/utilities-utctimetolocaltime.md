---
description: Converte Coordinated Universal Time (ora di Greenwich) nell'ora locale del computer.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Metodo Utilities.UTCTimeToLocalTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c1ad7236564fff2f9a3814beda9bedacbf96fbc9ca2678546304ee108891bea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005149"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Metodo Utilities.UTCTimeToLocalTime

\[Il **metodo UTCTimeToLocalTime** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.\]

Il **metodo UTCTimeToLocalTime** converte Coordinated Universal Time (ora di Greenwich) nell'ora locale del computer.

## <a name="syntax"></a>Sintassi


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UTCTime* \[ Pollici\]
</dt> <dd>

La Coordinated Universal Time da convertire nell'ora locale del computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Ora locale corrispondente all'oggetto Coordinated Universal Time.

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

 

 




