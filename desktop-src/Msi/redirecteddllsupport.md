---
description: Il programma di installazione imposta la proprietà RedirectedDLLSupport se la piattaforma di sistema che esegue l'installazione supporta Componenti isolati.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Proprietà RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24da5990645d4c27120c3a010cc517475ba6e706c2fb41d69a024d15ca524549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979321"
---
# <a name="redirecteddllsupport-property"></a>Proprietà RedirectedDLLSupport

Il programma di installazione imposta **la proprietà RedirectedDLLSupport** se la piattaforma di sistema che esegue l'installazione supporta [Componenti isolati](isolated-components.md).

Il programma di installazione imposta la **proprietà RedirectedDLLSupport** su un valore pari a 1 se il sistema che esegue l'installazione supporta [componenti](isolated-components.md) isolati basati su . File LOCAL. Il programma di installazione imposta la **proprietà RedirectedDLLSupport** su un valore pari a 2 se il sistema che esegue l'installazione supporta l'isolamento tramite . File LOCAL o assembly side-by-side Win32.

La **proprietà RedirectedDLLSupport** può essere usata per condizionare l'azione [IsolateComponents](isolatecomponents-action.md) nella tabella [InstallUISequence](installuisequence-table.md) o [InstallExecuteSequence](installexecutesequence-table.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




