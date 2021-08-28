---
description: L'azione ADVERTISE è un'azione di primo livello chiamata per installare o rimuovere i componenti annunciati.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: AZIONE ADVERTISE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd70b36edfb0074911ee3c9487a299f3c0b2eb4bacc59f05241fc6ee22119800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045931"
---
# <a name="advertise-action"></a>AZIONE ADVERTISE

L'azione ADVERTISE è un'azione di primo livello chiamata per installare o rimuovere i componenti annunciati.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

[*La*](a-gly.md) pubblicità si riferisce alla capacità del programma di installazione di fornire le interfacce di caricamento e avvio di un'applicazione senza installare fisicamente l'applicazione. Il programma di installazione non installa i componenti necessari finché un utente o un'applicazione non attiva un'interfaccia annunciata. Questo concetto è denominato [*install-on-demand.*](i-gly.md)

L'azione ADVERTISE non viene chiamata dall'interno della sequenza di tabella delle azioni, il programma di installazione di Windows esegue questa azione quando l'eseguibile della riga di comando Msiexec.exe viene chiamato con l'opzione della riga di comando '/j' o quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) viene chiamato con il parametro *szCommandLine* impostato su ACTION=ADVERTISE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella AdvtExecuteSequence](advtexecutesequence-table.md)
</dt> </dl>

 

 



