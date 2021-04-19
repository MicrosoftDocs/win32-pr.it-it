---
description: Questo esempio illustra come localizzare il pacchetto di Windows Installer descritto in un esempio di installazione. Il pacchetto di installazione originale viene modificato da una versione in lingua inglese a quella francese.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Esempio di localizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311104"
---
# <a name="a-localization-example"></a>Esempio di localizzazione

Questo esempio illustra come localizzare il pacchetto di Windows Installer descritto in [un esempio di installazione](an-installation-example.md). Il pacchetto di installazione originale viene modificato da una versione in lingua inglese a quella francese.

L'esempio di localizzazione presenta le specifiche seguenti:

-   L'interfaccia utente di installazione per l'applicazione MNP2000 deve essere modificata da inglese a francese.
-   La versione francese di MNP2000 include Readme.txt e Help.txt file scritti in lingua francese.
-   La versione francese include un elenco di agenti di viaggio in Francia che possono fornire biglietti a Red Park Arena. Questo elenco (fornito come nuovo file, Fre.txt) non fa parte della versione in lingua inglese.

La procedura generale per la localizzazione di un'installazione di è descritta nella sezione [localizzazione di un pacchetto di Windows Installer](localizing-a-windows-installer-package.md).

Copiare la versione in lingua inglese di MNP2000.msi e tutti i file di origine descritti in [pianificazione dell'installazione](planning-the-installation.md) in una nuova cartella. Modificare il nome del MNP2000.msi nella cartella MNPFren.msi. Nelle sezioni seguenti verrà modificata questa copia per localizzare l'applicazione in francese.

[Continua](checking-the-installation-database-code-page.md)

 

 



