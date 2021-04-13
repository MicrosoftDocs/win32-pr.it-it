---
title: Registrazione multimediale
description: Registrazione multimediale
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- MCIWndCreate (funzione)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395918"
---
# <a name="multimedia-recording"></a>Registrazione multimediale

È possibile implementare le funzionalità di registrazione nell'applicazione usando l'interfaccia utente incorporata in MCIWnd. È possibile utilizzare la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) per fornire controlli per l'avvio e l'arresto della registrazione e per il salvataggio delle informazioni registrate. Utilizzando **MCIWndCreate**, è possibile specificare gli stili della finestra per visualizzare una finestra di MCIWnd e includere il pulsante **record** sulla barra degli strumenti. Usando **MCIWndNew**, è possibile specificare il tipo di dispositivo da registrare e specificare che le informazioni devono essere acquisite in un nuovo file.

Se l'applicazione richiede una maggiore complessità, è possibile automatizzare e personalizzare la registrazione usando la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) . Per ulteriori informazioni, vedere [personalizzazione del processo di registrazione](customizing-the-recording-process.md).

> [!Note]  
> Alcuni dispositivi, ad esempio CD audio e MCIAVI, vengono usati solo per la riproduzione. Per la registrazione, è possibile usare altri dispositivi, ad esempio dispositivi audio waveform. Se si specifica un dispositivo che non è in grado di registrare, MCIWnd omette il pulsante **record** dalla barra degli strumenti.

 

 

 




