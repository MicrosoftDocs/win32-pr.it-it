---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRequired su una stringa che rappresenta il numero totale di byte richiesti da tutte le funzionalità selezionate nel volume a cui fa riferimento la proprietà PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: PrimaryVolumeSpaceRequired - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c644c53b5a36c8ba834a52c22ca3ba2b192499cbf351f122d8ed2b6a66a57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042261"
---
# <a name="primaryvolumespacerequired-property"></a>PrimaryVolumeSpaceRequired - proprietà

Il programma di installazione imposta il valore della **proprietà PrimaryVolumeSpaceRequired** su una stringa che rappresenta il numero totale di byte richiesti da tutte le funzionalità selezionate nel volume a cui fa riferimento la [**proprietà PrimaryVolumePath.**](primaryvolumepath.md) Come per la [**proprietà PrimaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) questo numero è espresso in unità di 512 byte.

## <a name="remarks"></a>Commenti

Si noti che se questo valore deve essere visualizzato all'interno di un controllo [Text](text-control.md)statico, il bit [FormatSize](formatsize-control-attribute.md) può essere usato per formattare e assegnare automaticamente un'etichetta a questo numero in unità di kilobyte o megabyte in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




