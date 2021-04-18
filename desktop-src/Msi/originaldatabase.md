---
description: Il Windows Installer imposta la proprietà OriginalDatabase sul percorso del database di installazione utilizzato per avviare l'installazione.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Proprietà OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327802"
---
# <a name="originaldatabase-property"></a>Proprietà OriginalDatabase

Il Windows Installer imposta la proprietà **OriginalDatabase** sul percorso del database di installazione utilizzato per avviare l'installazione. Se l'installazione viene avviata da una riga di comando, il valore varia a seconda che l'opzione di recaching Package (il flag-v) sia presente nella proprietà [**REINSTALLMODE**](reinstallmode.md) .



| Metodo di installazione                                                                                                                                                                                  | Valore OriginalDatabase                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Qualsiasi installazione avviata richiamando il percorso del pacchetto di installazione (file MSI).                                                                                                              | Percorso del pacchetto di installazione (file MSI). |
| Installazione avviata da una riga di comando. L'installazione non è stata avviata da un percorso del pacchetto. L'opzione recache (flag-v) è presente nella proprietà [**REINSTALLMODE**](reinstallmode.md) .     | Percorso del database nell'origine.           |
| Installazione avviata da una riga di comando. L'installazione non è stata avviata da un percorso del pacchetto. L'opzione recache (flag-v) non è presente nella proprietà [**REINSTALLMODE**](reinstallmode.md) . | Percorso del database memorizzato nella cache.                  |



 

## <a name="remarks"></a>Commenti

Durante la prima installazione, un'azione personalizzata sequenziata prima dell' [azione ResolveSource](resolvesource-action.md) può utilizzare la proprietà **OriginalDatabase** per determinare il percorso dell'origine di installazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




