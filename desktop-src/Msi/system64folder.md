---
description: Il programma di installazione imposta la proprietà System64Folder sul percorso completo della cartella system64 predefinita. La proprietà System64Folder esistente è impostata sulla cartella a 32 bit corrispondente.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Proprietà System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332934"
---
# <a name="system64folder-property"></a>Proprietà System64Folder

Il programma di installazione imposta la proprietà **System64Folder** sul percorso completo della cartella system64 predefinita. La proprietà **System64Folder** esistente è impostata sulla cartella a 32 bit corrispondente.

## <a name="remarks"></a>Commenti

Il programma di installazione imposta questa proprietà su Windows a 64 bit. Ad esempio, in Windows a 64 bit, il valore può essere C: \\ Window \\ system32. Questa proprietà non viene utilizzata in Windows a 32 bit.

Questa cartella è in genere una sottodirectory della cartella Windows. Tuttavia, si trova in un server se configurato per le finestre condivise.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




