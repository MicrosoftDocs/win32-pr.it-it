---
description: Restituisce una rappresentazione di stringa dei dati codificati.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Metodo EncodedData.Format
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b3d4316a2de24410a14d496b71e46746ea580109f8d6ede10c4c1a0f57fc22f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874871"
---
# <a name="encodeddataformat-method"></a>Metodo EncodedData.Format

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) nello spazio [**dei nomi System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Il **metodo Format** restituisce una rappresentazione di stringa dei dati codificati.

## <a name="syntax"></a>Sintassi


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bMultiLines* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se la stringa restituita contiene più righe. Se **True,** la stringa restituita può contenere più righe separate da **vbCrLf.** Il valore predefinito è **False**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa leggibile che rappresenta i dati codificati. Se CAPICOM non comprende i dati codificati, viene restituita una rappresentazione esadecimale dei dati.

## <a name="remarks"></a>Commenti

Il formato della stringa restituita può cambiare tra versioni diverse di CAPICOM. Non fare affidamento su un formato specifico nell'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EncodedData**](encodeddata.md)
</dt> </dl>

 

 
