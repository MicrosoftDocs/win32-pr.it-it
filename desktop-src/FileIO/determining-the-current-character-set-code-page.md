---
description: La funzione AreFileApisANSI determina se le funzioni di I/O dei file utilizzano la tabella codici del set di caratteri ANSI o OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinazione della tabella codici del set di caratteri corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882189"
---
# <a name="determining-the-current-character-set-code-page"></a>Determinazione della tabella codici del set di caratteri corrente

La funzione [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se le funzioni di i/O dei file utilizzano la tabella codici del set di caratteri ANSI o OEM. La funzione [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) fa sì che le funzioni usino la tabella codici ANSI. La funzione [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) fa sì che le funzioni usino la tabella codici OEM.

Per impostazione predefinita, le funzioni di I/O dei file usano i nomi file ANSI. Le funzioni esportate da Kernel32.dll che accettano o restituiscono nomi di file sono interessate dall'impostazione della tabella codici del file.

Sia [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) che [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) impostano la tabella codici per processo, anziché per thread o per computer.

 

 



