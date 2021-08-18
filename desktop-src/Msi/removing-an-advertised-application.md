---
description: Per rimuovere un'applicazione installata nello stato annunciato, è sufficiente disinstallarla usando MsiInstallProduct o MsiConfigureProduct. È anche possibile rimuovere un'applicazione annunciata dalla riga di comando. Vedere Opzioni della riga di comando.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Rimozione di un'applicazione annunciata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880ce7d7de7ce7a8f9c9a20511f3f9d1b48ccdf34ffd2da51a71d226d0770b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041581"
---
# <a name="removing-an-advertised-application"></a>Rimozione di un'applicazione annunciata

Per rimuovere un'applicazione installata nello stato annunciato, è sufficiente disinstallarla usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). È anche possibile rimuovere un'applicazione annunciata dalla riga di comando. Vedere [Opzioni della riga di comando](command-line-options.md).

Si noti che potrebbe non essere possibile rimuovere un'applicazione annunciata se il pacchetto è stato creato in modo che l'esecuzione di un'installazione sia condizionale in base **all'istruzione NOT Installed**. Un'applicazione annunciata non è installata nel computer dell'utente e il programma di installazione non imposta la [**proprietà Installed.**](installed.md) Il pacchetto deve essere creato in modo che le applicazioni annunciate possano essere disinstallate.

 

 



