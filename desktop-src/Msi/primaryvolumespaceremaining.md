---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRemaining su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà PrimaryVolumePath, se tutte le funzionalità attualmente selezionate sono state installate.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Proprietà PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333672"
---
# <a name="primaryvolumespaceremaining-property"></a>Proprietà PrimaryVolumeSpaceRemaining

Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceRemaining** su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) , se tutte le funzionalità attualmente selezionate sono state installate. Come per la proprietà [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , questo numero è espresso in unità di 512 byte.

## <a name="remarks"></a>Commenti

Nota Se questo valore deve essere visualizzato in un [controllo testo](text-control.md)statico, il bit [FormatSize](formatsize-control-attribute.md) può essere usato per formattare automaticamente ed etichettare questo numero in unità di kilobyte o megabyte, a seconda dei casi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




