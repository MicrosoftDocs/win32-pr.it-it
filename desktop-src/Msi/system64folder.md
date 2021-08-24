---
description: Il programma di installazione imposta la proprietà System64Folder sul percorso completo della cartella System64 predefinita. La proprietà System64Folder esistente viene impostata sulla cartella a 32 bit corrispondente.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d586451ab596f5b480c74f382659596128a12c041596dec3c530b18307af2820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500431"
---
# <a name="system64folder-property"></a>System64Folder - proprietà

Il programma di installazione **imposta la proprietà System64Folder** sul percorso completo della cartella System64 predefinita. La proprietà **System64Folder esistente** viene impostata sulla cartella a 32 bit corrispondente.

## <a name="remarks"></a>Commenti

Il programma di installazione imposta questa proprietà su un Windows a 64 bit. Ad esempio, in un Windows a 64 bit il valore può essere C: \\ Window \\ System32. Questa proprietà non viene usata nelle applicazioni a 32 bit Windows.

Questa cartella è in genere una sottodirectory della Windows cartella. Tuttavia, si trova in un server quando è configurato per l'Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




