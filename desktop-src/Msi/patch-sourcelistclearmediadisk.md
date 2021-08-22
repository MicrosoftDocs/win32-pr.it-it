---
description: Il metodo SourceListClearMediaDisk dell'oggetto Patch rimuove un disco specificato dal set di dischi registrati per una patch. Accetta Diskid come parametro. Questo metodo chiama MsiSourceListClearMediaDisk.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Metodo Patch.SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73f3303ae8521dd5fb87f17a685189770d17de2d0289f0801b81fef5332b5076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558541"
---
# <a name="patchsourcelistclearmediadisk-method"></a>Metodo Patch.SourceListClearMediaDisk

Il **metodo SourceListClearMediaDisk** dell'oggetto [**Patch**](patch-object.md) rimuove un disco specificato dal set di dischi registrati per una patch. Accetta *Diskid* come parametro. Questo metodo chiama [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).

## <a name="syntax"></a>Sintassi


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Diskid* 
</dt> <dd>

Questo parametro fornisce l'ID del disco da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IPatch IID è definito come \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




