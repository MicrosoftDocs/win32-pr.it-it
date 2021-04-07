---
description: Descrive le operazioni di reparse point che è possibile eseguire usando DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Operazioni di reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058042"
---
# <a name="reparse-point-operations"></a>Operazioni di reparse point

Per determinare se un file system supporta i reparse point, chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il file supporta il flag di bit **\_ \_ reparse \_ Point** .

La funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) consente di impostare, modificare, ottenere e rimuovere i reparse point. Nella tabella seguente vengono descritte le operazioni di reparse point che è possibile eseguire utilizzando **DeviceIoControl**.



| Operazione                                                           | Descrizione                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**FSCTL \_ set \_ reparse \_ Point**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | Consente al programma chiamante di impostare un nuovo punto di analisi o di modificarne uno esistente.<br/> |
| [**FSCTL \_ ottenere un \_ punto di analisi \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | Ottiene le informazioni archiviate in un punto di analisi esistente.<br/>                         |
| [**FSCTL \_ Elimina \_ punto di analisi \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | Rimuove un punto di analisi esistente.<br/>                                                   |



 

Se si sta modificando, recuperando o eliminando un punto di analisi, è necessario specificare lo stesso tag di reparse nell'operazione contenuta nel file. In caso contrario, l'operazione avrà esito negativo e si verificherà un **errore di \_ reparse \_ tag non \_ corrispondente**. Se si sta modificando o eliminando un punto di analisi, è necessario specificare anche il **GUID** di reparse nell'operazione contenuta nel file. In caso contrario, l'operazione avrà esito negativo e si verificherà un conflitto di errore di **\_ reparse \_ Attribute \_**.

Per determinare se un file o una directory contiene un reparse point, utilizzare la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) . Se al file o alla directory è associato un reparse point, viene impostato l'attributo **\_ \_ reparse \_ Point dell'attributo file** .

Per sovrascrivere un reparse point esistente senza avere già un handle per il file o la directory, chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il **flag di file \_ \_ aperto \_ reparse \_ Point**. Questo flag consente di aprire il file indipendentemente dal fatto che il filtro file system corrispondente sia installato e funzioni correttamente.

 

