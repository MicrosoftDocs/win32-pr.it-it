---
description: L'azione annuncia è un'azione di primo livello chiamata per installare o rimuovere i componenti annunciati.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Pubblicizza azione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756245"
---
# <a name="advertise-action"></a>Pubblicizza azione

L'azione annuncia è un'azione di primo livello chiamata per installare o rimuovere i componenti annunciati.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Per [*annuncio*](a-gly.md) si intende la capacità del programma di installazione di fornire le interfacce di caricamento e avvio di un'applicazione senza installare fisicamente l'applicazione. Il programma di installazione non installa i componenti necessari fino a quando un utente o un'applicazione non attiva un'interfaccia annunciata. Questo concetto viene definito [*installazione su richiesta*](i-gly.md).

L'azione ADVERTISe non viene chiamata dall'interno della sequenza della tabella Action, il Windows Installer esegue questa azione quando l'eseguibile della riga di comando Msiexec.exe viene chiamato con l'opzione della riga di comando '/j ' o quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) viene chiamato con il parametro *SZCOMMANDLINE* impostato su Action = advertise.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella AdvtExecuteSequence](advtexecutesequence-table.md)
</dt> </dl>

 

 



