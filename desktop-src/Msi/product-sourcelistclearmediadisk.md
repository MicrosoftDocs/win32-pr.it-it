---
description: Il metodo SourceListClearMediaDisk dell'oggetto Product rimuove un disco specificato dal set di dischi registrati per un prodotto. Accetta DiskID come parametro. Questo metodo chiama MsiSourceListClearMediaDisk.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Metodo Product. SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325881"
---
# <a name="productsourcelistclearmediadisk-method"></a>Metodo Product. SourceListClearMediaDisk

Il metodo **SourceListClearMediaDisk** dell'oggetto [**Product**](product-object.md) rimuove un disco specificato dal set di dischi registrati per un prodotto. Accetta *DiskID* come parametro. Questo metodo chiama [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).

## <a name="syntax"></a>Sintassi


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DiskID* 
</dt> <dd>

Questo parametro fornisce l'ID del disco da rimuovere.

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

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




