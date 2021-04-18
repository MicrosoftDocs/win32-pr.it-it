---
description: Il programma di installazione imposta la proprietà TempFolder sul percorso completo della cartella Temp. Gli autori non devono necessariamente impostare la proprietà TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Proprietà TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324917"
---
# <a name="tempfolder-property"></a>Proprietà TempFolder

Il programma di installazione imposta la proprietà **TempFolder** sul percorso completo della cartella Temp.

Gli autori non devono necessariamente impostare la proprietà **TempFolder** . Windows Installer usa la funzione [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) per recuperare il percorso della directory designata per i file temporanei e per impostare questa proprietà.

## <a name="remarks"></a>Commenti

Un valore comune per questa proprietà è C: \\ Temp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
