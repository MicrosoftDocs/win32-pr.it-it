---
description: La funzione AreFileApisANSI determina se le funzioni di I/O di file usano la tabella codici del set di caratteri ANSI o OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinazione della tabella codici del set di caratteri corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18361c0553407ade59c2d1de61ac2fb20d18d5b9d46018bcbc74dc3a114917b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150658"
---
# <a name="determining-the-current-character-set-code-page"></a>Determinazione della tabella codici del set di caratteri corrente

La [**funzione AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se le funzioni di I/O di file usano la tabella codici del set di caratteri ANSI o OEM. La [**funzione SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) fa in modo che le funzioni usino la tabella codici ANSI. La [**funzione SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) fa in modo che le funzioni usino la tabella codici OEM.

Per impostazione predefinita, le funzioni di I/O di file usano nomi di file ANSI. Le funzioni esportate da Kernel32.dll che accettano o restituiscono nomi di file sono interessate dall'impostazione della tabella codici del file.

Sia [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) che [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) impostano la tabella codici per processo, anziché per thread o per computer.

 

 



