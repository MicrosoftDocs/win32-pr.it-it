---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceAvailable su una stringa che rappresenta il numero totale di byte disponibili, in unità di 512, nel volume a cui fa riferimento la proprietà PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Proprietà PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327801"
---
# <a name="primaryvolumespaceavailable-property"></a>Proprietà PrimaryVolumeSpaceAvailable

Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceAvailable** su una stringa che rappresenta il numero totale di byte disponibili, in unità di 512, nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) .

## <a name="remarks"></a>Commenti

Ad esempio, se [**PrimaryVolumePath**](primaryvolumepath.md) è impostato su "D:" e volume D: include 446.134.272 byte disponibili, **PrimaryVolumeSpaceAvailable** viene impostato su 871356.

Nota Se questo valore deve essere visualizzato in un [controllo testo](text-control.md)statico, il bit [FormatSize](formatsize-control-attribute.md) può essere usato per formattare automaticamente ed etichettare questo numero in unità di kilobyte o megabyte, a seconda dei casi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




