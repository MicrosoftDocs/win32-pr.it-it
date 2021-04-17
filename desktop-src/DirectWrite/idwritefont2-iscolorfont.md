---
title: Metodo IDWriteFont2 IsColorFont
description: Consente di determinare se un percorso di rendering del colore è potenzialmente necessario.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Scrittura diretta metodo IsColorFont
- Metodo IsColorFont scrittura diretta, interfaccia IDWriteFont2
- IDWriteFont2 Interface Direct Write, metodo IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400756"
---
# <a name="idwritefont2iscolorfont-method"></a>Metodo IDWriteFont2:: IsColorFont

Consente di determinare se un percorso di rendering del colore è potenzialmente necessario.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce **true** se il tipo di carattere contiene informazioni sui colori (tabelle colr e CPAL); in caso contrario, **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





