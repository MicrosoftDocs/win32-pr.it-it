---
title: Metodo IDWriteFont2 IsColorFont
description: Consente di determinare se un percorso di rendering dei colori è potenzialmente necessario.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Metodo IsColorFont Direct Write
- Metodo IsColorFont Direct Write, interfaccia IDWriteFont2
- Metodo IsColorFont dell'interfaccia IDWriteFont2 Direct Write
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
ms.openlocfilehash: 144aded290c7a4121dd785a1844971e3c1b5501b8ae78707d8da5378c44b002a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650185"
---
# <a name="idwritefont2iscolorfont-method"></a>Metodo IDWriteFont2::IsColorFont

Consente di determinare se un percorso di rendering dei colori è potenzialmente necessario.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

Restituisce **TRUE se** il tipo di carattere contiene informazioni sul colore (tabelle COLR e CPAL); in caso **contrario, FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





