---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceAvailable su una stringa che rappresenta il numero totale di byte disponibili, in unità di 512, nel volume a cui fa riferimento la proprietà PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: PrimaryVolumeSpaceAvailable - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9336bfa32ebb3bf0c12b7e7fc54ddad2b26cd635c820ca6e8ea2caabe163ceb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580671"
---
# <a name="primaryvolumespaceavailable-property"></a>PrimaryVolumeSpaceAvailable - proprietà

Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceAvailable** su una stringa che rappresenta il numero totale di byte disponibili, in unità di 512, nel volume a cui fa riferimento la [**proprietà PrimaryVolumePath.**](primaryvolumepath.md)

## <a name="remarks"></a>Commenti

Ad esempio, se [**PrimaryVolumePath**](primaryvolumepath.md) è impostato su "D:" e il volume D: ha 446.134.272 byte liberi, **PrimaryVolumeSpaceAvailable** è impostato su 871356.

Si noti che se questo valore deve essere visualizzato all'interno di un controllo [Text](text-control.md)statico, è possibile usare il bit [FormatSize](formatsize-control-attribute.md) per formattare e assegnare automaticamente un'etichetta a questo numero in unità di kilobyte o megabyte in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




