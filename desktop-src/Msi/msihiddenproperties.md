---
description: È possibile utilizzare la proprietà MsiHiddenProperties per impedire al programma di installazione di visualizzare le password o altre informazioni riservate nel file di log.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Proprietà MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329249"
---
# <a name="msihiddenproperties-property"></a>Proprietà MsiHiddenProperties

È possibile utilizzare la proprietà **MsiHiddenProperties** per impedire al programma di installazione di visualizzare le password o altre informazioni riservate nel file di log. Per impedire che una proprietà venga scritta nel file di log, impostare il valore della proprietà **MsiHiddenProperties** sul nome della proprietà che si desidera nascondere. È possibile nascondere più proprietà specificando una stringa di nomi di proprietà delimitati da punti e virgola (;).

> [!Note]  
> Quando il criterio di [debug](debug.md) è impostato su un valore pari a 7, il programma di installazione scriverà le informazioni immesse in una riga di comando nel log. In questo modo le proprietà pubbliche immesse in una riga di comando risultano visibili anche se la proprietà è inclusa nella proprietà **MsiHiddenProperties** . In questo modo, le informazioni riservate possono essere inserite in una riga di comando visibile nel log. Per ulteriori informazioni, vedere [impedire che le informazioni riservate vengano scritte nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




