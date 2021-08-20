---
description: Il programma di installazione imposta la proprietà SystemFolder sul percorso completo della cartella System.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: SystemFolder - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1567942e981af161654d41988ef797b64116af5cdb25e07a3d4f1465fc4ce975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142009"
---
# <a name="systemfolder-property"></a>SystemFolder - proprietà

Il programma di installazione imposta **la proprietà SystemFolder** sul percorso completo della cartella System.

## <a name="remarks"></a>Commenti

Il programma di installazione imposta questa proprietà. Ad esempio, in un Windows a 32 bit il valore può essere C: \\ Windows \\ System32. Nelle applicazioni a 64 bit Windows, il valore può essere C: \\ Windows \\ SysWow64.

Questa cartella è in genere una sottodirectory della Windows cartella. Tuttavia, si trova in un server quando è configurato per l'Windows.

Questa cartella è locale, anche se configurata per l'Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




