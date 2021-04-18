---
description: La proprietà MediaDisks enumera tutti i dischi multimediali per questa istanza del prodotto. Questa proprietà chiama MsiSourceListEnumMediaDisks. Restituisce le informazioni sul disco come matrice di oggetti record.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Proprietà patch. MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324773"
---
# <a name="patchmediadisks-property"></a>Proprietà patch. MediaDisks

La proprietà **MediaDisks** enumera tutti i dischi multimediali per questa istanza del prodotto. Questa proprietà chiama [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa). Restituisce le informazioni sul disco come matrice di oggetti [**record**](record-object.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

In ogni record il primo campo contiene l'ID disco, il secondo campo contiene l'etichetta del volume e il terzo campo contiene il prompt del disco registrato per il disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[**Registra**](record-object.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




