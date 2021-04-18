---
description: La proprietà Products è una proprietà di sola lettura che restituisce un oggetto String enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Proprietà Installer. Products
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328316"
---
# <a name="installerproducts-property"></a>Proprietà Installer. Products

La proprietà **Products** è una proprietà di sola lettura che restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per enumerare i prodotti, un'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto. Poiché i prodotti non sono ordinati, qualsiasi nuovo prodotto dispone di un indice arbitrario. Ciò significa che la funzione può restituire prodotti in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




