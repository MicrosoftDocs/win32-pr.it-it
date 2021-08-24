---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRemaining su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà PrimaryVolumePath, se sono state installate tutte le funzionalità attualmente selezionate.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: PrimaryVolumeSpaceRemaining - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16107af105de0684bd917177050017a3c14e40aff32c658881342a90e877c973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580491"
---
# <a name="primaryvolumespaceremaining-property"></a>PrimaryVolumeSpaceRemaining - proprietà

Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceRemaining** su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath,**](primaryvolumepath.md) se sono state installate tutte le funzionalità attualmente selezionate. Come per la [**proprietà PrimaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) questo numero è espresso in unità di 512 byte.

## <a name="remarks"></a>Commenti

Si noti che se questo valore deve essere visualizzato all'interno di un controllo [Text](text-control.md)statico, è possibile usare il bit [FormatSize](formatsize-control-attribute.md) per formattare e assegnare automaticamente un'etichetta a questo numero in unità di kilobyte o megabyte in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




