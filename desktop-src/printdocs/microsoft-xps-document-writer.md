---
description: Il Microsoft XPS Document Writer (MXDW) è un driver di stampa su file che consente a un'applicazione Windows di creare file di documento XML Paper Specification (XPS) nelle versioni di Windows a partire da Windows XP con Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS Document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba69a6efff4f2da0ab0cc03bdc71468dada14c457de7685053096d2fba672d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938887"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Microsoft XPS Document Writer (MXDW)

Il Microsoft XPS Document Writer (MXDW) è un driver di stampa su file che consente a un'applicazione Windows di creare file di documento XML Paper Specification (XPS) nelle versioni di Windows a partire da Windows XP con Service Pack 2 (SP2). L'uso di MXDW consente a un'applicazione Windows di salvare il contenuto come documento XPS senza modificare il codice del programma dell'applicazione.

## <a name="when-to-use"></a>Utilizzo

L'utente seleziona MXDW quando vuole creare un documento XPS da un'applicazione Windows che non ha la possibilità di salvare il contenuto come documento XPS.

Gli sviluppatori di applicazioni consigliano l'MXDW agli utenti che vogliono creare documenti XPS quando l'applicazione non offre la possibilità di salvare come documento XPS. Per altre informazioni sui documenti XML Paper Specification e XPS, vedere XML Paper Specification [e](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) XPS Specification and License Downloads ( Download delle licenze e delle specifiche [XPS).](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)

MXDW viene installato automaticamente in Windows Vista e versioni successive di Windows e può essere scaricato e installato in Windows XP con SP2 e Windows Server 2003.

## <a name="installation"></a>Installazione

In Windows Vista e versioni successive di Windows, MXDW viene installato automaticamente quando viene installato il sistema operativo.

**Windows XP con SP2 e Windows Server 2003:** scaricare e installare .NET Framework 3.0 o XPS Essential Pack dall'Area [download Microsoft](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Uso

Una volta installato, MXDW viene visualizzato come coda di stampa disponibile nella finestra di dialogo Stampa presentata da un'applicazione. Quando si seleziona MXDW come stampante, all'utente viene richiesto di specificare il nome file da creare come documento XPS che acquisisce l'output di stampa dell'applicazione.

L'immagine seguente mostra l'MXDW selezionato come stampante nella finestra Windows di stampa comune di Vista.

![immagine della finestra di dialogo di stampa che mostra la selezione di microsoft xps document writer (mxdw)](images/choosingmxdwinvista.gif)

Gli sviluppatori di applicazioni possono personalizzare l'output di MXDW usando le [impostazioni di configurazione di MXDW.](mxdw-configuration-settings.md)

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

 

 
