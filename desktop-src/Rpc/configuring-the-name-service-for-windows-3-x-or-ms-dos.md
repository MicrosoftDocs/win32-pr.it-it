---
title: Configurazione del servizio dei nomi per Windows 3.x o MS-DOS
description: Chiamata di procedura remota (RPC) e configurazione del servizio dei nomi per Windows 3.x o MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24884c782913c47806c702ff129594c6524fe7c0e731561de405f3b6a360c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022431"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Configurazione del servizio dei nomi per Windows 3.x o MS-DOS

Quando si esegue Setup.exe per installare la libreria di runtime RPC a 16 bit, viene richiesto di selezionare un provider di servizi dei nomi:

-   Se si sceglie Installa provider di servizi dei nomi **predefinito,** viene installato il provider di servizi di rete predefinito, Microsoft Locator.
-   Se si sceglie Installa provider di  servizi di **nomi** personalizzati, completare la finestra di dialogo Definisci indirizzo di rete per installare dce cell directory service come provider di servizi di rete. DcE Cell Directory Service è il provider di servizi di rete usato con i server DCE.

L'indirizzo di rete è il nome del computer host che esegue il daemon NSI (nsid). Questo computer funge da gateway per dce cell directory service, passando chiamate di funzione NSI tra computer che eseguono sistemi operativi Microsoft e computer DCE. L'indirizzo di rete può contenere al massimo 80 caratteri, ad esempio 11.1.9.169 è un indirizzo valido.

 

 




