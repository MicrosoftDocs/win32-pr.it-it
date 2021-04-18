---
description: La funzione BuildINIPath restituisce il percorso completo di un file INI che corrisponde alle informazioni immesse.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Funzione BuildINIPath (Netmon. h)
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
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314186"
---
# <a name="buildinipath-function"></a>BuildINIPath (funzione)

La funzione **BuildINIPath** restituisce il percorso completo di un file ini che corrisponde alle informazioni immesse.

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

Buffer che riceve il nome completo del file INI.

</dd> <dt>

*IniFileName* 
</dt> <dd>

Nome del file INI (il nome file completo meno l'estensione filename).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore al nome completo del file INI.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Il percorso restituito da questa funzione è il percorso completo di un file INI che corrisponde alle informazioni immesse. Se ad esempio si immette XNS o TCP, la funzione genera un percorso rispettivamente per Xns.ini o Tcp.ini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




