---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilità DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320643"
---
# <a name="depnx-compatibility"></a>Compatibilità DEP/NX

Per impostazione predefinita, in Windows Internet Explorer 7, DEP/NX è disabilitato per motivi di compatibilità. Diversi componenti aggiuntivi diffusi non sono compatibili con DEP/NX e non riescono quando Windows Internet Explorer li carica con DEP/NX abilitato.

In genere, questi componenti aggiuntivi vengono compilati utilizzando una versione precedente di ATL Framework. ATL 7,1 e versioni precedenti non sono progettati con la funzionalità di protezione DEP. Fortunatamente, le nuove versioni di Microsoft Windows Service Pack hanno nuove API DEP/NX che consentono di utilizzare DEP/NX e mantenere la compatibilità con le versioni precedenti di ATL. Queste nuove API consentono a Internet Explorer di scegliere DEP/NX senza causare l'esito negativo dei componenti aggiuntivi compilati utilizzando versioni precedenti di ATL.

Quando un componente aggiuntivo non è compatibile con DEP/NX e non utilizza un oggetto ATL obsoleto, è possibile utilizzare un'opzione di Criteri di gruppo per rifiutare esplicitamente DEP/NX per Internet Explorer fino a quando non viene distribuita una versione aggiornata del controllo non funzionante. Gli amministratori locali possono controllare DEP/NX eseguendo Internet Explorer come amministratore e deselezionando l'opzione **Abilita protezione della memoria** nel riquadro **Avanzate** di **Opzioni Internet**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
