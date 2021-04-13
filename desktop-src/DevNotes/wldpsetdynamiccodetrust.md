---
description: Imposta una attendibilità del codice dinamico di .NET CRL su disco per .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Funzione WldpSetDynamicCodeTrust (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401410"
---
# <a name="wldpsetdynamiccodetrust-function"></a>WldpSetDynamicCodeTrust (funzione)

Imposta una attendibilità del codice dinamico di .NET CRL su disco per .NET.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileHandle* 
</dt> <dd>

Handle per un file di codice dinamico su disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1803 \[\]<br/>                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




