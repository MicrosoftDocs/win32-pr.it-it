---
description: Converte l'ora locale del computer in Coordinated Universal Time (ora di Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Utilities. LocalTimeToUTCTime, metodo
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
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323942"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Utilities. LocalTimeToUTCTime, metodo

\[Il metodo **LocalTimeToUTCTime** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]

Il metodo **LocalTimeToUTCTime** converte l'ora locale del computer in Coordinated Universal Time (ora di Greenwich).

## <a name="syntax"></a>Sintassi


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Localtime* \[ in\]
</dt> <dd>

Ora locale da convertire nell'ora UTC (Coordinated Universal Time).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Ora UTC (Coordinated Universal Time) corrispondente all'ora locale specificata.

## <a name="remarks"></a>Commenti

Sebbene il sistema usi internamente l'ora UTC (Coordinated Universal Time), in genere le applicazioni visualizzano l'ora locale, ovvero la data e l'ora del giorno per il fuso orario locale del computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Utilità**](utilities.md)
</dt> </dl>

 

 




