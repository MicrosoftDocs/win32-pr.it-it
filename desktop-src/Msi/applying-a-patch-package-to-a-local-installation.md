---
description: È possibile applicare il piccolo aggiornamento a un'installazione locale di MNP2000 con la patch di esempio MNPpatch. msp creata per generare un pacchetto di patch.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Applicazione di un pacchetto di patch a un'installazione locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227215"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>Applicazione di un pacchetto di patch a un'installazione locale

È possibile applicare il piccolo aggiornamento a un'installazione locale di MNP2000 con la patch di esempio MNPpatch. msp creata per [generare un pacchetto di patch](generating-a-patch-package.md). La procedura generale è illustrata nella sezione [applicazione di piccoli aggiornamenti applicando patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md).

Installare il prodotto MNP2000 originale localmente nel computer. Verificare che sia presente l'errore Concert.txt che la correzione del piccolo aggiornamento sia stata completata. Avviare quindi l'installazione immettendo la riga di comando seguente.

**msiexec/p MNP2000. msp REINSTALL = ALL REINSTALLMODE = omus**

Esaminare nuovamente i Concert.txt appartenenti a MNP2000 per verificare che il programma di installazione abbia applicato il piccolo aggiornamento per correggere il file.

Per applicare il piccolo aggiornamento a un'immagine amministrativa, vedere [applicazione di un pacchetto di patch a un'installazione amministrativa](applying-a-patch-package-to-an-administrative-installation.md).

[Continua](applying-a-patch-package-to-an-administrative-installation.md)

 

 



