---
description: Quando le applicazioni esistenti diventano datate o non vengono più usate, potrebbe essere necessario rimuoverle.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eliminazione di un'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8332cd59ecde4115daa43ea97bc87d4354338e3ea94073317bfa293102deb78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047509"
---
# <a name="deleting-a-com-application"></a>Eliminazione di un'applicazione COM+

Quando le applicazioni esistenti diventano datate o non vengono più usate, potrebbe essere necessario rimuoverle.

**Per eliminare un'applicazione COM+**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer per il quale si desidera eliminare un'applicazione.

2.  Aprire la **cartella Applicazioni COM+** per il computer specificato per visualizzare tutte le applicazioni.

3.  Selezionare l'applicazione da rimuovere.

4.  Se è stata selezionata un'applicazione server, arrestare l'applicazione. È possibile arrestare un'applicazione selezionandola nello strumento di amministrazione Servizi componenti, facendo clic con il pulsante destro del mouse e quindi **scegliendo Arresta**. Se è stata selezionata un'applicazione di libreria, assicurarsi che tutti i processi che usano questa applicazione di libreria siano arrestati.

5.  Scegliere **Elimina** dal menu **Azione.** È anche possibile fare clic con il pulsante destro del mouse sul nome dell'applicazione e quindi scegliere **Elimina.** È anche possibile eliminare un'applicazione selezionandola nello strumento  di amministrazione Servizi componenti e premendo CANC oppure è possibile selezionare l'applicazione, fare clic con il pulsante destro del mouse e quindi scegliere **Elimina.**

6.  Fare **clic su Sì** quando viene richiesto di confermare l'azione.

Inoltre, se un'applicazione server o un proxy di applicazione è stato installato in un computer usando il programma di installazione di Windows (come descritto in "Installazione di applicazioni COM+" nella Guida all'amministrazione di Servizi componenti), è possibile eliminarlo tramite l'utilità Installazione applicazioni in Microsoft Windows Pannello di controllo. Oppure è possibile eliminare un'applicazione server installata o un proxy di applicazione usando la sintassi della riga di Windows Installer:

**msiexec -x** *application \_ name***.msi**

Questi metodi sono particolarmente utili per l'eliminazione di applicazioni COM+ in computer client che non eseguono lo strumento di amministrazione Servizi componenti.

L'eliminazione dell'applicazione elimina anche tutti i componenti contenuti nell'applicazione. Se questi componenti dipendono da risorse aggiuntive (connessioni di database, file di dati o di testo, configurazione della radice virtuale IIS e così via), queste risorse devono essere rimosse tramite meccanismi diversi da Servizi componenti.

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

 

 



