---
description: Recupera un rettangolo che rappresenta l'area di input massima della tavoletta.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'Metodo ITablet:: GetMaxInputRect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883742"
---
# <a name="itabletgetmaxinputrect-method"></a>Metodo ITablet:: GetMaxInputRect

Recupera un rettangolo che rappresenta l'area di input massima della tavoletta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*prcInput* \[ out\]
</dt> <dd>

Puntatore al rettangolo che rappresenta l'area di input massima della tavoletta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> </dl>

 

 




