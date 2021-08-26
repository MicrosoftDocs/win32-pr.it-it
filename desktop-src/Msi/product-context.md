---
description: La proprietà Context restituisce il contesto di questo prodotto.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Product.Context - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21fb23a595b1f479f2468f0006cca7cd9218de03fc2cc76b794caae79ea45a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129121"
---
# <a name="productcontext-property"></a>Product.Context - proprietà

La **proprietà Context** restituisce il contesto di questo prodotto.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Product.Context
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa proprietà può restituire uno dei valori seguenti.



| Context                        | Valore | Significato                           |
|--------------------------------|-------|-----------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | Prodotti nel contesto gestito.   |
| UTENTE \_ MSIINSTALLCONTEXT        | 2     | Prodotti nel contesto non gestito. |
| COMPUTER \_ MSIINSTALLCONTEXT     | 4     | Prodotti nel contesto del computer.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




