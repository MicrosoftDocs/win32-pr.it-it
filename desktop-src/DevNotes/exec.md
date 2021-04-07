---
description: HKLM \\ software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748759"
---
# <a name="exec"></a>Exec

**HKLM \\ software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Tipo di dati | Range                    | Valore predefinito |
|-----------|--------------------------|---------------|
| REG \_ SZ   | *Percorso del file eseguibile* |               |



 

## <a name="browser-integration-steps"></a>Passaggi di integrazione del browser

1.  Usare la funzione [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) per determinare se la diagnostica di rete è installata. Se è installato, la chiave **{e2e2dd38-d088-4134-82b7-f2ba38496583}** è presente.
2.  Usare la funzione [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) per recuperare il percorso del file eseguibile di diagnostica di rete dalla voce **Exec** .
3.  Visualizza la pagina nuovo errore se la diagnostica è installata nel sistema.
4.  Creare un'estensione del browser che crei una voce della barra degli strumenti standard se la diagnostica è installata nel sistema.
5.  Eseguire l'eseguibile di diagnostica di rete usando il percorso recuperato nel passaggio 2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica delle funzionalità degli strumenti di diagnostica di rete](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
