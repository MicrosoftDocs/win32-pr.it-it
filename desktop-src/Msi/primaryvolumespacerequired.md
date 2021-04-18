---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRequired su una stringa che rappresenta il numero totale di byte necessari per tutte le funzionalità selezionate nel volume a cui fa riferimento la proprietà PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Proprietà PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333673"
---
# <a name="primaryvolumespacerequired-property"></a>Proprietà PrimaryVolumeSpaceRequired

Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceRequired** su una stringa che rappresenta il numero totale di byte necessari per tutte le funzionalità selezionate nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) . Come per la proprietà [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , questo numero è espresso in unità di 512 byte.

## <a name="remarks"></a>Commenti

Nota Se questo valore deve essere visualizzato in un [controllo testo](text-control.md)statico, il bit [FormatSize](formatsize-control-attribute.md) può essere usato per formattare automaticamente ed etichettare questo numero in unità di kilobyte o megabyte, a seconda dei casi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




