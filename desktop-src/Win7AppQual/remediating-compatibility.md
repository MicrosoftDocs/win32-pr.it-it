---
description: Compatibilità DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilità DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116429"
---
# <a name="depnx-compatibility"></a>Compatibilità DEP/NX

Per impostazione predefinita, in Windows Internet Explorer 7 DEP/NX è disabilitato per motivi di compatibilità. Diversi componenti aggiuntivi più diffusi non sono compatibili con DEP/NX e hanno esito negativo quando Windows Internet Explorer li carica con DEP/NX abilitato.

In genere, questi componenti aggiuntivi vengono compilati usando una versione precedente del framework ATL. ATL 7.1 e versioni precedenti non sono progettati con la funzionalità di sicurezza DEP. Fortunatamente, le nuove versioni dei Service Pack di Microsoft Windows hanno nuove API DEP/NX che consentono di usare DEP/NX e di mantenere la compatibilità con le versioni precedenti di ATL. Queste nuove API consentono Internet Explorer di acconsentire esplicitamente a DEP/NX senza causare errori nei componenti aggiuntivi compilati con versioni precedenti di ATL.

Quando un componente aggiuntivo non è compatibile con DEP/NX e non usa un atl obsoleto, è possibile usare un'opzione Criteri di gruppo per rifiutare esplicitamente DEP/NX per Internet Explorer fino a quando non viene distribuita una versione aggiornata del controllo interrotto. Gli amministratori locali possono controllare DEP/NX eseguendo Internet Explorer come amministratore  e deselezionando  l'opzione Abilita protezione memoria nel riquadro Avanzate di **Opzioni Internet**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
