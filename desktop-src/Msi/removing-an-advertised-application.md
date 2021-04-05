---
description: Per rimuovere un'applicazione installata nello stato pubblicizzato, è sufficiente disinstallarla usando MsiInstallProduct o MsiConfigureProduct. È anche possibile rimuovere un'applicazione annunciata dalla riga di comando. Vedere Opzioni della riga di comando.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Rimozione di un'applicazione annunciata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882721"
---
# <a name="removing-an-advertised-application"></a>Rimozione di un'applicazione annunciata

Per rimuovere un'applicazione installata nello stato pubblicizzato, è sufficiente disinstallarla usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). È anche possibile rimuovere un'applicazione annunciata dalla riga di comando. Vedere [Opzioni della riga di comando](command-line-options.md).

Si noti che potrebbe non essere possibile rimuovere un'applicazione annunciata se il pacchetto è stato creato in modo tale che l'esecuzione di un'installazione è condizionale quando l'istruzione **non è installata**. Un'applicazione annunciata non è installata nel computer dell'utente e il programma di installazione non imposta la proprietà [**installata**](installed.md) . Il pacchetto deve essere creato in modo che sia possibile disinstallare le applicazioni annunciate.

 

 



