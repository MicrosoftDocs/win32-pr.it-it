---
description: La proprietà RelatedProducts di sola lettura restituisce un oggetto String enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti con una proprietà UpgradeCode specificata nella tabella delle proprietà.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Proprietà Installer. RelatedProducts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332167"
---
# <a name="installerrelatedproducts-property"></a>Proprietà Installer. RelatedProducts

La proprietà **RelatedProducts** di sola lettura restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti con una proprietà [**UpgradeCode**](upgradecode.md) specificata nella [tabella delle proprietà](property-table.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Valore proprietà

Codice di aggiornamento dei prodotti correlati enumerati dal programma di installazione.

## <a name="remarks"></a>Commenti

Per enumerare i prodotti correlati, un'applicazione scorre la [**stringa**](stringlist-object.md) usando un oggetto per ogni costrutto. Poiché i prodotti correlati non sono ordinati, qualsiasi nuovo prodotto correlato ha un indice arbitrario. Ciò significa che la funzione può restituire prodotti correlati in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




