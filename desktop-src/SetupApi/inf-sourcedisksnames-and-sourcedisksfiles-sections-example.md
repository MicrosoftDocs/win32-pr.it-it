---
description: La sezione SourceDisksNames di un file INF identifica i dischi che contengono i file di origine da installare.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Esempio di sezioni INF SourceDisksNames e SourceDisksFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315323"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Esempio di sezioni INF SourceDisksNames e SourceDisksFiles

La sezione **SourceDisksNames** di un file inf identifica i dischi che contengono i file di origine da installare. La sezione **SourceDisksFiles** identifica i file di origine e i dischi di origine che li contengono. Si noti che le piattaforme MIPS, Alpha e PPC non sono supportate da Windows 2000 o Windows XP.

A partire da Windows XP, una sezione **SourceDisksNames** può specificare un tag e un file CAB. Ad esempio, la sezione **SourceDisksNames** seguente può essere utilizzata con supporti rimovibili o fissi. Se si usa un supporto rimovibile, nella sezione di esempio viene verificata la presenza del supporto controllando prima di tutto la presenza del tag. Se si usa un supporto fisso, nella sezione di esempio viene verificata la presenza del supporto controllando prima di tutto la presenza del cabinet. Dopo aver verificato la presenza di un file CAB, il sistema tenta di copiare i file all'esterno dell'archivio e di richiedere eventuali file che non sono stati copiati.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Per ulteriori informazioni su **SourceDisksNames** o **SourceDisksFiles**, vedere le sezioni "linee guida generali per file inf" e "sezioni e DIRETTIVe dei file inf" del Microsoft Windows 2000 Driver Development Kit.

 

 



