---
description: Il metodo SourceListClearSource rimuove un'origine di rete o URL. Accetta il tipo, il tipo di origine e SourcePath, il percorso di origine, come parametri da rimuovere. Questo metodo chiama MsiSourceListClearSource.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Metodo Product. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325880"
---
# <a name="productsourcelistclearsource-method"></a>Metodo Product. SourceListClearSource

Il metodo **SourceListClearSource** rimuove un'origine di rete o URL. Accetta il *tipo*, il tipo di origine e *SourcePath*, il percorso di origine, come parametri da rimuovere. Questo metodo chiama [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).

## <a name="syntax"></a>Sintassi


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo di origine da rimuovere: MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Percorso dell'origine da rimuovere.

</dd> </dl>

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

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




