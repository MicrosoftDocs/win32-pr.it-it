---
description: Compatibilità DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilità DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af83e43defb5216b176755dbc8f32067f907620bc120a16aff8b6db3392c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329626"
---
# <a name="depnx-compatibility"></a>Compatibilità DEP/NX

Per impostazione predefinita, in Windows Internet Explorer 7 DEP/NX è disabilitato per motivi di compatibilità. Diversi componenti aggiuntivi più diffusi non sono compatibili con DEP/NX e hanno esito negativo quando Windows Internet Explorer li carica con DEP/NX abilitato.

In genere, questi componenti aggiuntivi vengono compilati usando una versione precedente del framework ATL. ATL 7.1 e versioni precedenti non sono progettati con la funzionalità di sicurezza DEP. Fortunatamente, le nuove versioni dei Service Pack di Microsoft Windows hanno nuove API DEP/NX che consentono di usare DEP/NX e mantenere la compatibilità con le versioni precedenti di ATL. Queste nuove API consentono Internet Explorer di acconsentire esplicitamente a DEP/NX senza causare l'esito negativo dei componenti aggiuntivi compilati usando versioni precedenti di ATL.

Quando un componente aggiuntivo non è compatibile con DEP/NX e non usa un ATL obsoleto, è possibile usare un'opzione Criteri di gruppo per rifiutare esplicitamente DEP/NX per Internet Explorer fino a quando non viene distribuita una versione aggiornata del controllo interrotto. Gli amministratori locali possono controllare DEP/NX eseguendo Internet Explorer come amministratore  e deselezionando l'opzione Abilita protezione memoria nel **riquadro** Avanzate di **Opzioni Internet.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
