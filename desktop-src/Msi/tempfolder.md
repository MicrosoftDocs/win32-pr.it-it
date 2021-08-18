---
description: Il programma di installazione imposta la proprietà TempFolder sul percorso completo della cartella Temp. Gli autori non devono impostare la proprietà TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: TempFolder - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5ded141982c12204eb5267357cedded6521eccb7cc47a3bf000b026faf9aed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626507"
---
# <a name="tempfolder-property"></a>TempFolder - proprietà

Il programma di installazione **imposta la proprietà TempFolder** sul percorso completo della cartella Temp.

Gli autori non devono impostare la **proprietà TempFolder.** Windows Il programma di [**installazione usa la funzione GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) per recuperare il percorso della directory designata per i file temporanei e impostare questa proprietà.

## <a name="remarks"></a>Commenti

Un valore comune per questa proprietà è C: \\ Temp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
