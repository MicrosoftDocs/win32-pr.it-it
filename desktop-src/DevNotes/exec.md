---
description: HKLM \\ Software Microsoft Internet Explorer Extensions \\ \\ \\ \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93228857af2e531360b6238ab649daf8ac3f9eb2acf0aecfb12348b0ed990b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795241"
---
# <a name="exec"></a>Exec

**HKLM \\ Software Microsoft Internet Explorer Extensions \\ \\ \\ \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Tipo di dati | Range                    | Valore predefinito |
|-----------|--------------------------|---------------|
| REG \_ SZ   | *Percorso del file eseguibile* |               |



 

## <a name="browser-integration-steps"></a>Passaggi di integrazione del browser

1.  Usare la [**funzione RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) per determinare se Diagnostica di rete è installato. Se è installato, è presente la chiave **{e2e2dd38-d088-4134-82b7-f2ba38496583}.**
2.  Usare la [**funzione RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) per recuperare il percorso del file eseguibile di Diagnostica di rete dalla **voce Exec.**
3.  Visualizzare la nuova pagina di errore se la diagnostica è installata nel sistema.
4.  Creare un'estensione del browser che crea un elemento standard della barra degli strumenti se la diagnostica è installata nel sistema.
5.  Eseguire il file eseguibile di Diagnostica di rete usando il percorso recuperato nel passaggio 2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica della funzionalità Strumenti di diagnostica di rete](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
