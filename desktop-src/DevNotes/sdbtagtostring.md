---
description: Recupera il nome visualizzato del TAG specificato.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483124"
---
# <a name="sdbtagtostring-function"></a>SdbTagToString (funzione)

Recupera il nome visualizzato del TAG specificato.

## <a name="syntax"></a>Sintassi


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tag* \[ di in\]
</dt> <dd>

TAG.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un puntatore alla stringa con terminazione null o a "InvalidTag".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TAG**](tag.md)
</dt> </dl>

 

 




