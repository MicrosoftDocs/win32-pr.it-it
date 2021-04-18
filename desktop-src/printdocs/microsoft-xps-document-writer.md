---
description: Microsoft XPS Document Writer (MXDW) è un driver di stampa per file che consente a un'applicazione Windows di creare file di documento XPS (XML Paper Specification) nelle versioni di Windows a partire da Windows XP con Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS Document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318362"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Microsoft XPS Document Writer (MXDW)

Microsoft XPS Document Writer (MXDW) è un driver di stampa per file che consente a un'applicazione Windows di creare file di documento XPS (XML Paper Specification) nelle versioni di Windows a partire da Windows XP con Service Pack 2 (SP2). L'uso di MXDW consente a un'applicazione Windows di salvare il contenuto come documento XPS senza modificare il codice programma dell'applicazione.

## <a name="when-to-use"></a>Utilizzo

Quando si desidera creare un documento XPS da un'applicazione Windows che non è in grado di salvare il contenuto come documento XPS, è necessario selezionare il MXDW di un utente.

Gli sviluppatori di applicazioni possono consigliare MXDW agli utenti che desiderano creare documenti XPS quando l'applicazione non offre la possibilità di salvare un documento XPS. Per ulteriori informazioni sulla specifica del documento XML e sui documenti XPS, vedere [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) e [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

MXDW viene installato automaticamente in Windows Vista e nelle versioni successive di Windows e può essere scaricato e installato in Windows XP con SP2 e Windows Server 2003.

## <a name="installation"></a>Installazione

In Windows Vista e nelle versioni successive di Windows, MXDW viene installato automaticamente quando viene installato il sistema operativo.

**Windows XP con SP2 e Windows Server 2003**: scaricare e installare .net Framework 3,0 o XPS Essential Pack dall' [area download Microsoft](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Uso

Quando è installato, il MXDW viene visualizzato come una coda di stampa disponibile nella finestra di dialogo Stampa presentata da un'applicazione. Quando MXDW viene selezionato come stampante, all'utente viene richiesto il nome del file da creare come documento XPS che acquisisce l'output di stampa dell'applicazione.

Nella figura seguente viene illustrato il MXDW selezionato come stampante nella finestra di dialogo Stampa comune di Windows Vista.

![immagine della finestra di dialogo stampa che mostra la selezione di Microsoft XPS Document Writer (MXDW)](images/choosingmxdwinvista.gif)

Gli sviluppatori di applicazioni possono personalizzare l'output di MXDW usando le [impostazioni di configurazione di MXDW](mxdw-configuration-settings.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Specifiche XPS e download delle licenze](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Strumento di conformità isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[Impostazioni di configurazione di MXDW](mxdw-configuration-settings.md)
</dt> </dl>

 

 
