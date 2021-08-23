---
description: La proprietà Sources enumera tutte le origini per l'istanza del prodotto.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Product.Sources - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c54b9563898b093af324b02ca6a5bf48fbddf62b31c22a3d492c1132c46f13f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753921"
---
# <a name="productsources-property"></a>Product.Sources - proprietà

La **proprietà Sources** enumera tutte le origini per l'istanza del prodotto. Questa proprietà chiama [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) e restituisce la matrice di stringhe e accetta il tipo di origine come argomento. Il tipo di origine può essere MSISOURCETYPE \_ NETWORK o MSISOURCETYPE \_ URL.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a>Valore proprietà

Tipo di origine da enumerare. Il valore può essere *msiInstallSourceTypeNetwork* (1) o *msiInstallSourceTypeURL* (2).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Installer 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




