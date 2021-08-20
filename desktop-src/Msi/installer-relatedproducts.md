---
description: La proprietà RelatedProducts di sola lettura restituisce un oggetto StringList che enumera il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti con una proprietà UpgradeCode specificata nella tabella Property.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Installer.RelatedProducts - proprietà
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
ms.openlocfilehash: 15e84a063b8f094dbeee02f3000bdd1c69356f5fa664f6e6f6aff87d19d07dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946139"
---
# <a name="installerrelatedproducts-property"></a>Installer.RelatedProducts - proprietà

La proprietà **RelatedProducts** di sola lettura restituisce un oggetto [**StringList**](stringlist-object.md) che enumera il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti con una proprietà [**UpgradeCode**](upgradecode.md) specificata nella tabella [Property](property-table.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Valore proprietà

Codice di aggiornamento dei prodotti correlati enumerati dal programma di installazione.

## <a name="remarks"></a>Commenti

Per enumerare i prodotti correlati, un'applicazione esegue l'iterazione di [**StringList**](stringlist-object.md) usando un costrutto For Each. Poiché i prodotti correlati non vengono ordinati, i nuovi prodotti correlati hanno un indice arbitrario. Ciò significa che la funzione può restituire prodotti correlati in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




