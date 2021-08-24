---
description: La funzione BuildINIPath restituisce un percorso completo di un file INI che corrisponde alle informazioni immesse.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Funzione BuildINIPath (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b75df338142ab0ec97db3e60cbba1b5f68df3e0e67947d4c13cdccccd409bdf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744692"
---
# <a name="buildinipath-function"></a>Funzione BuildINIPath

La **funzione BuildINIPath** restituisce un percorso completo di un file INI che corrisponde alle informazioni immesse.

## <a name="syntax"></a>Sintassi


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FullPath* 
</dt> <dd>

Buffer che riceve il nome file INI completo.

</dd> <dt>

*IniFileName* 
</dt> <dd>

Nome del file INI (il nome completo del file meno l'estensione del nome file).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore al nome file INI completo.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Il percorso restituito da questa funzione è un percorso completo di un file INI che corrisponde alle informazioni immesse. Ad esempio, se si immette XNS o TCP, la funzione genera un percorso Xns.ini o Tcp.ini, rispettivamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




