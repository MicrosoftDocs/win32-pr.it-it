---
description: Poiché le applicazioni esistenti diventano obsolete o non vengono più utilizzate, potrebbe essere necessario rimuoverle.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eliminazione di un'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401464"
---
# <a name="deleting-a-com-application"></a>Eliminazione di un'applicazione COM+

Poiché le applicazioni esistenti diventano obsolete o non vengono più utilizzate, potrebbe essere necessario rimuoverle.

**Per eliminare un'applicazione COM+**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer per cui si desidera eliminare un'applicazione.

2.  Aprire la cartella **applicazioni com+** per il computer specificato per visualizzare tutte le applicazioni.

3.  Selezionare l'applicazione che si desidera rimuovere.

4.  Se è stata selezionata un'applicazione server, arrestare l'applicazione. Per arrestare un'applicazione, è possibile selezionarla nello strumento di amministrazione Servizi componenti, fare clic con il pulsante destro del mouse e quindi scegliere **Arresta**. Se è stata selezionata un'applicazione libreria, assicurarsi che tutti i processi che attualmente utilizzano questa applicazione di libreria vengano arrestati.

5.  Scegliere **Elimina** dal menu **azione** . È anche possibile fare clic con il pulsante destro del mouse sul nome dell'applicazione e quindi scegliere **Elimina**. Per eliminare un'applicazione, è anche possibile selezionarla nello strumento di amministrazione Servizi componenti e premere il tasto **Canc** oppure selezionare l'applicazione, fare clic con il pulsante destro del mouse e scegliere **Elimina**.

6.  Quando viene richiesto di confermare l'azione, fare clic su **Sì** .

Inoltre, se un'applicazione server o un proxy di applicazione è stato installato in un computer utilizzando Windows Installer (come descritto in "installazione di applicazioni COM+" nella Guida all'amministrazione di Servizi componenti), è possibile eliminarlo tramite l'utilità Installazione applicazioni nel pannello di controllo di Microsoft Windows. In alternativa, è possibile eliminare un'applicazione server o un proxy di applicazione installato utilizzando la sintassi della riga di comando Windows Installer:

**msiexec-x** *\_ nome applicazione * * *. msi**

Questi metodi sono particolarmente utili per eliminare le applicazioni COM+ nei computer client che non eseguono lo strumento di amministrazione Servizi componenti.

Eliminando l'applicazione vengono eliminati anche tutti i componenti contenuti nell'applicazione. Se questi componenti dipendono da risorse aggiuntive (connessioni di database, file di dati o di testo, configurazione della radice virtuale di IIS e così via), queste risorse devono essere rimosse tramite meccanismi diversi dallo strumento di amministrazione Servizi componenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Copia di componenti](copying-components.md)
</dt> <dt>

[Creazione di una nuova applicazione COM+](creating-a-new-com--application.md)
</dt> <dt>

[Importazione di componenti](importing-components.md)
</dt> <dt>

[Installazione di nuovi componenti](installing-new-components.md)
</dt> <dt>

[Spostamento dei componenti](moving-components.md)
</dt> <dt>

[Rimozione di un componente da un'applicazione COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



