---
description: La proprietà state restituisce lo stato di installazione dell'istanza del prodotto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Proprietà Product. state
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330622"
---
# <a name="productstate-property"></a>Proprietà Product. state

La proprietà **state** restituisce lo stato di installazione dell'istanza del prodotto.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa proprietà restituisce uno dei valori seguenti.



| Stato di installazione       | Significato                                |
|--------------------------|----------------------------------------|
| \_impostazione predefinita InstallState    | Istanza del prodotto installata localmente. |
| INSTALLSTATE \_ annunciata | Istanza del prodotto annunciata.        |
| INSTALLSTATE \_ sconosciuto    | Istanza del prodotto sconosciuta.           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




