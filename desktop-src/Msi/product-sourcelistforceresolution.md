---
description: Il metodo SourceListForceResolution Cancella la proprietà LastUsedSource.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Metodo Product. SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330628"
---
# <a name="productsourcelistforceresolution-method"></a>Metodo Product. SourceListForceResolution

Il metodo **SourceListForceResolution** Cancella la proprietà LastUsedSource. In questo modo, il programma di installazione esegue la ricerca nell'elenco di origine di una fonte di prodotto valida la volta successiva che è richiesta un'origine, ad esempio quando il programma di installazione esegue un'installazione o una reinstallazione o quando il percorso è necessario per l'esecuzione di un componente dall'origine.

Questo metodo chiama [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).

## <a name="syntax"></a>Sintassi


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

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

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




