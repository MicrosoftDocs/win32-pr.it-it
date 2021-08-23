---
description: La proprietà MsiHiddenProperties può essere usata per impedire al programma di installazione di visualizzare password o altre informazioni riservate nel file di log.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: MsiHiddenProperties - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acea21b946a4169748c96970143d6c44c6bf682ce6f6a8e4624791c52d0ba813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628106"
---
# <a name="msihiddenproperties-property"></a>MsiHiddenProperties - proprietà

La **proprietà MsiHiddenProperties** può essere usata per impedire al programma di installazione di visualizzare password o altre informazioni riservate nel file di log. Per impedire la scrittura di una proprietà nel file di log, impostare il valore della proprietà **MsiHiddenProperties** sul nome della proprietà che si vuole nascondere. È possibile nascondere più proprietà specificando una stringa di nomi di proprietà delimitati da punti e virgola (;).

> [!Note]  
> Quando i [criteri di](debug.md) debug sono impostati su un valore pari a 7, il programma di installazione scriverà le informazioni immesse in una riga di comando nel log. In questo modo le proprietà pubbliche immesse in una riga di comando sono visibili anche se la proprietà è inclusa nella **proprietà MsiHiddenProperties.** In questo modo le informazioni riservate immesse in una riga di comando possono essere visualizzate nel log. Per altre informazioni, vedere [Impedisci](preventing-confidential-information-from-being-written-into-the-log-file.md)la scrittura di informazioni riservate nel file di log.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




