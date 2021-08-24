---
description: Il metodo SourceListForceResolution cancella la proprietà LastUsedSource.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Metodo Product.SourceListForceResolution
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
ms.openlocfilehash: 3215f5b43200cb8ca43fba36dc71e1a582aa24b92904e2c48268245921a2ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754011"
---
# <a name="productsourcelistforceresolution-method"></a>Metodo Product.SourceListForceResolution

Il **metodo SourceListForceResolution** cancella la proprietà LastUsedSource. In questo modo il programma di installazione cerca nell'elenco di origine un'origine del prodotto valida alla successiva richiesta di un'origine, ad esempio quando il programma di installazione esegue un'installazione o una reinstallazione o quando il percorso è necessario per l'esecuzione di un set di componenti dall'origine.

Questo metodo chiama [**MsiSourceListForceResolution.**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)

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
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




