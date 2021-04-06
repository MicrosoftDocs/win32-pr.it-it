---
title: Configurazione del servizio nome per Windows 3. x o MS-DOS
description: RPC (Remote Procedure Call) e configurazione del servizio nome per Windows 3. x o MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044870"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Configurazione del servizio nome per Windows 3. x o MS-DOS

Quando si esegue Setup.exe per installare la libreria di runtime RPC a 16 bit, viene richiesto di selezionare un provider di servizi dei nomi:

-   Se si sceglie **install default name service provider**, viene installato il valore predefinito NSP, Microsoft Locator.
-   Se si sceglie **Installa provider di servizi nome personalizzato**, completare la finestra di dialogo **Definisci indirizzo di rete** per installare il servizio directory di celle DCE come NSP. Il servizio directory di celle DCE è il NSP usato con i server DCE.

L'indirizzo di rete è il nome del computer host che esegue il daemon NSI (NSID). Questo computer funge da gateway per il servizio directory celle DCE, passando le chiamate di funzione NSI tra computer che eseguono sistemi operativi Microsoft e computer DCE. L'indirizzo di rete non può contenere più di 80 caratteri, ad esempio 11.1.9.169 è un indirizzo valido.

 

 




